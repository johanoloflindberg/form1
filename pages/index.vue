<template>
  <main>
    <div class="intro">
      <h1>Nuxt Toolbox</h1>
      <p>
        Hi 👋! This template gives you a
        <a href="https://nuxtjs.org/">Nuxt</a> app with the scaffolding for
        <a href="https://www.netlify.com/products/functions/"
          >Netlify Functions</a
        >, <a href="https://www.netlify.com/products/forms/">Forms</a>, and
        <a href="https://docs.netlify.com/routing/redirects/">Redirects</a>. Our
        aim was to give you the code you would need to hit the ground running
        with a few fun features.
      </p>

      <form name="contact" method="POST" data-netlify="true">
  <input type="hidden" name="form-name" value="contact" />
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />
  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4" required></textarea>
  <button type="submit">Submit</button>
</form>

      <p>
        You can find the code for this project on GitHub at
        <a href="https://github.com/netlify-templates/nuxt-toolbox"
          >https://github.com/netlify-templates/nuxt-toolbox</a
        >! Happy coding!
      </p>
    </div>
    <FeedbackForm />
    <JokeBlock />
  </main>
</template>

<style>
* {
  font-family: 'Helvetica', sans-serif;
}
.intro {
  min-width: 400px;
  padding: 10px 40px;
  width: 60%;
}
</style>

<script>
  document.querySelector('form[name="contact"]').addEventListener('submit', function (e) {
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;

    if (!name || !email) {
      alert('Name and Email are required fields.');
      e.preventDefault(); // Prevent form submission
    }
  });
</script>
