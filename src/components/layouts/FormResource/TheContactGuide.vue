<template>
  <div class="contact-container__guide">
    <header class="guide-header__container">
      <h1 class="guide-title">
        <slot name="title"></slot>
      </h1>

      <p class="guide-description">
        <slot name="description"></slot>
      </p>
    </header>
    <!--description navs-->
    <nav>
      <ul>
        <li>
          <div class="svg-container">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="feather feather-phone"
            >
              <path
                d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"
              ></path>
            </svg>
          </div>
          <div class="svg-description__container">
            <p>+0123 4567 8910</p>
          </div>
        </li>
        <li>
          <div class="svg-container">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="feather feather-mail"
            >
              <path
                d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
              ></path>
              <polyline points="22,6 12,13 2,6"></polyline>
            </svg>
          </div>
          <div class="svg-description__container">
            <p>email@gmail.com</p>
          </div>
        </li>
        <li>
          <div class="svg-container">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="48"
              height="48"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="feather feather-map-pin"
            >
              <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
              <circle cx="12" cy="10" r="3"></circle>
            </svg>
          </div>
          <div class="svg-description__container">
            <p>102 Street 2714 Don</p>
          </div>
        </li>
      </ul>
    </nav>
    <!--footer-->
    <footer class="guide-footer__container">
      <div class="footer-socialIcon_container">
        <div class="social-icon">
    
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="48"
            height="48"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-twitter"
          >
            <path
              d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"
            ></path>
          </svg>
        </div>
        <div class="social-icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="48"
            height="48"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-facebook"
          >
            <path
              d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"
            ></path>
          </svg>
        </div>
        <div class="social-icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="48"
            height="48"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-instagram"
          >
            <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
            <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
            <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
          </svg>
        </div>
        <div class="social-icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="48"
            height="48"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-linkedin"
          >
            <path
              d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
            ></path>
            <rect x="2" y="9" width="4" height="12"></rect>
            <circle cx="4" cy="4" r="2"></circle>
          </svg>
        </div>
      </div>
      <!--bubbles -->
      <div class="footer-bubble_container first-bubble">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="48"
          height="48"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-circle"
        >
          <circle cx="12" cy="12" r="10"></circle>
        </svg>
      </div>
      <div class="footer-bubble_container second-bubble">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="48"
          height="48"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-circle"
        >
          <circle cx="12" cy="12" r="10"></circle>
        </svg>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  props: ["title", "description"],
  data() {
    return {};
  },
};
</script>

<style scoped>
div.contact-container__guide {
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  width: 400px;
  height: 500px;
  max-width: 450px;
  min-width: 400px;
  background-color: var(--primaryColor);
  border-radius: 10px;
}
header.guide-header__container {
  display: flex;
  flex-direction: column;
  width: 100%;
  justify-content: center;
  align-content: flex-start;
  padding: 2rem;
}
header.guide-header__container h1 {
  color: white;
  font-family: inherit;
  font-size: 1.5rem;
  margin: 0;
  padding: 0px;
  width: 100%;
}
header.guide-header__container p {
  color: var(--secondaryColor);
  font-family: "Karla", sans-serif;
  font-size: 1rem;
  text-align: justify;
}
ul {
  display: flex;
  flex-direction: column;
  width: 100%;
  list-style-type: none;
  padding: 0;
  margin-top: 0;
}
li {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: space-between;
  padding: 0.5rem 2rem;
}
li div {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-right: 1.4rem;
}
svg.feather {
  color: var(--primaryColor);
  width: 1.4rem;
  height: 1.4rem;
  fill: var(--accentColor);
  stroke-width: thin;
}

footer {
  position: relative;
}
div.footer-bubble_container {
  position: absolute;
}
div.first-bubble {
  right: -131px;
  top: -61px;
}
div.second-bubble {
  right: 72px;
  top: -45px;
}
div.first-bubble svg {
  fill: var(--primaryBubbleColor);
  stroke-width: 0;
  width: 20rem;
  height: 20rem;
}
div.second-bubble svg {
  fill: var(--secondaryBubbleColor);
  stroke-width: 0;
  width: 8rem;
  height: 8rem;
}
div.footer-socialIcon_container{
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    position: absolute;
    bottom: -108px;
    width: 100%;
    padding:1rem;
}
div.social-icon{
    margin-right:1rem;
    border-radius: 100%;
    padding: 4px;
    display: flex;
    color: aliceblue;
    align-items: center;
    justify-content: center
}
div.social-icon svg{
    width:1rem;
    height: 1rem;
}
div.social-icon svg{
    cursor:pointer
}

div.social-icon:hover{
    background-color: pink;
}
li p {
  color: white;
  font-size: 1rem;
  font-family: "Karla", sans-serif;
  line-height: 1.2rem;
  width: 100%;
  opacity: 0.8;
}
</style>
