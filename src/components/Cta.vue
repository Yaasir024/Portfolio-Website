<template>
<div class="contact reveal">
        <h3>Want Me To work on your new project?</h3>
        <h1>Contact Me</h1>
        <p>I'm open to new job oppurtunities currently. If you think I'm good enough to work on your next project or just want to say Hi, kindly send an E-mail to <a href="mailto:yope4ever@gmail.com" target="_blank">yope4ever@gmail.com</a></p>
        <button>
            <a href="mailto:yope4ever@gmail.com" target="_blank">Send A Message</a>
        </button>
    </div>
</template>

<style scoped>
.contact {
  max-width: 680px;
  margin: auto;
/* background: red; */
  margin-top: 150px;
  padding: 20px 15px;
  text-align: center;
  margin-bottom: 60px;
}
.contact h3 {
  font-size: 30px;
  font-style: italic;
}
.contact p {
  font-size: 16px;
  line-height: 25px;
  margin: 25px 0;
}
.contact p a {
  color: #fff;
  font-style: italic;
}
.contact p a:hover{
  font-style: normal;
}
button {
    background: none;
    padding: 8px 16px;
    margin: 10px 0;
    border: 2px solid var(--color-text-secondary);
    border-radius: 2px;
}
button a {
    font-weight: 600;
    font-size: 17px;
}
</style>