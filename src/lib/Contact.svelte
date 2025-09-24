<script>
  const FORM_ACCESS_KEY = "7610b07b-f839-460e-a505-0d0d613f5e24";
  const websiteURL = "https://website.com";
  const props = $props();
  const textContent = props.textContent;
</script>

<section id="contact" class="contact-section">
  <div class="contact-intro flex flex-col items-center">
    <h2 class="contact-title text-6xl">
      {textContent.contact.heading}
    </h2>
    <p class="contact-description">
      {textContent.contact.description}
    </p>
  </div>

  <form
    class="contact-form mb-24"
    action="https://api.web3forms.com/submit"
    method="POST"
  >
    <input type="hidden" name="access_key" value={FORM_ACCESS_KEY} />
    <input type="hidden" name="subject" value="Nouveau message" />
    <input
      type="hidden"
      name="from_name"
      value="Contact via webdev portfolio"
    />

    <div class="form-group-container">
      <div class="form-group">
        <label for="name" class="form-label"
          >{textContent.contact.name.label}</label
        >
        <input
          id="name"
          name="name"
          class="form-input"
          placeholder={textContent.contact.name.placeholder}
          type="text"
        />
      </div>
      <div class="form-group">
        <label for="email" class="form-label"
          >{textContent.contact.email.label} <span>*</span></label
        >
        <input
          required
          id="email"
          name="email"
          class="form-input"
          placeholder={textContent.contact.email.placeholder}
          type="email"
        />
      </div>
      <div class="form-group">
        <label for="message" class="form-label"
          >{textContent.contact.message.label} <span> *</span></label
        >
        <textarea
          required
          class="form-textarea"
          id="message"
          name="message"
          placeholder={textContent.contact.message.placeholder}
        ></textarea>
      </div>
    </div>
    <input type="hidden" name="redirect" value={websiteURL} />
    <button class="form-submit bg-primary" type="submit"
      >{textContent.contact.submit}</button
    >
  </form>
</section>

<style>
  .contact-section {
    width: 100%;
    max-width: 40rem;
    margin-left: auto;
    margin-right: auto;
    padding: 3rem 1rem;
  }

  .contact-intro > * + * {
    margin-top: 1rem;
  }

  .contact-description {
    color: rgb(107 114 128);
  }

  .form-group-container {
    display: grid;
    gap: 1rem;
    margin-top: 2rem;
  }

  .form-group {
    display: flex;
    flex-direction: column;
  }

  .form-label {
    margin-bottom: 0.5rem;
  }

  .form-input,
  .form-textarea {
    padding: 0.5rem;
    border: 1px solid #e5e7eb;
    display: flex;
    height: 2.5rem;
    width: 100%;
    border-radius: 0.375rem;
    font-size: 0.875rem;
    line-height: 1.25rem;
  }

  .form-input::placeholder,
  .form-textarea:focus-visible {
    color: #6b7280;
  }

  .form-input:focus-visible,
  .form-textarea:focus-visible {
    outline: 2px solid #2563eb;
    outline-offset: 2px;
  }

  .form-textarea {
    min-height: 120px;
  }

  .form-submit {
    width: 100%;
    margin-top: 1.2rem;
    color: #fff;
    padding: 13px 5px;
    border-radius: 0.375rem;
  }
</style>
