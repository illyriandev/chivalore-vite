<template>
  <div class="home">
    <NavBar site="home" />
    <section class="showcase flex">
      <div class="showcaseLogo">
        <img src="../assets/Logos/chivalore-logo.png" alt="Chivalore logo" />
      </div>
      <p class="showcaseText">chivalry<br />valor<br />lore.</p>
    </section>
    <section class="prosperism">
      <div class="prosperism-content flex">
        <p class="prosperism-header">
          The origin of Prosperism<br />and all Prosperist projects.
        </p>
        <div class="prosperism-definition">
          <img
            src="../assets/prosperism-definition.png"
            alt="Definition of Prosperism"
          />
        </div>
      </div>
    </section>
    <div class="transition journal-bg"></div>
    <section class="prosperist-journal">
      <div class="container flex">
        <div class="journal-logo flex">
          <img
            src="../assets/Logos/journal-logo.png"
            alt="Prosperist Journal Logo"
          />
        </div>
        <div class="journal-text flex">
          <p>
            Read the chapters that forge the philosophy of Prosperism on my blog
            - “Prosperist Journal”
          </p>
          <router-link class="link journal-bg" :to="{ name: 'Journal' }">
            > prosperist journal</router-link
          >
        </div>
      </div>
    </section>
    <section class="prosperist-projects">
      <div class="prosperist-projects-bg">
        <div class="container flex">
          <h1 class="journal-bg">The Prosperist Projects</h1>
          <ul class="flex">
            <li>Knight of Illyria</li>
            <li>Kingly Tales</li>
            <li>Neverland's Saviour</li>
            <li>The Path Realm</li>
            <li>Prosperist Journal</li>
          </ul>
        </div>
      </div>
    </section>
    <div class="transition home-bg"></div>
    <section class="contact">
      <div class="container flex">
        <form action="#" class="contact-form flex">
          <label>Write to me!</label>
          <input type="text" class="contact-input" placeholder="Name" />
          <input type="email" class="contact-input" placeholder="Email" />
          <textarea placeholder="Message" />
          <button type="submit">Send</button>
        </form>
        <div class="contact-svg flex">
          <Feather />
        </div>
      </div>
    </section>
    <HomeFooter />
  </div>
</template>

<script>
import NavBar from "../components/NavBar.vue";
import HomeFooter from "../components/HomeFooter.vue";
import Feather from "../assets/Icons/feather.svg"
export default {
  name: "HomeView",
  components: { NavBar, HomeFooter, Feather },
  setup() {},
};
</script>

<style lang="scss" scoped>
.home {
  position: relative;

  .showcase {
    width: 100%;
    height: 40vw;
    justify-content: center;
    padding-top: 12%;
    gap: 3vw;
    background: linear-gradient(
      0deg,
      rgba(227, 197, 172, 1) 0%,
      rgba(255, 255, 255, 1) 20%,
      rgba(255, 255, 255, 1) 80%,
      rgba(240, 226, 215, 1) 100%
    );
    clip-path: polygon(100% 0, 100% 100%, 50% 83%, 0 100%, 0 0);
    z-index: 2;
    user-select: none;

    .showcaseText {
      font-family: "Cormorant Unicase";
      color: #4a0025;
      font-weight: 700;
      line-height: 0.6;
      letter-spacing: -0.4vw;
      font-size: 9vw;
      width: 40%;
      padding-left: 3vw;
    }

    .showcaseLogo {
      width: 50%;

      img {
        width: 100%;
        height: auto;
      }
    }
  }

  .prosperism {
    position: relative;
    top: -165px;
    left: 0;
    width: 100%;
    height: auto;
    padding-bottom: 5rem;
    background-image: url("../assets/Images/books.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: top;
    z-index: -1;
    user-select: none;

    &::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background: rgba(0, 0, 0, 0.6);
    }

    .prosperism-content {
      position: relative;
      padding: 195px 1rem 0 1rem;
      height: 100%;
      color: #fff;
      font-family: "Spectral";
      font-style: italic;
      letter-spacing: -0.2vw;
      flex-direction: column;
      justify-content: center;
      align-content: center;
      gap: 2rem;
      text-shadow: 0px 1px 5px rgba(0, 0, 0, 0.6);
      line-height: 1.1;

      .prosperism-header {
        text-align: center;
        font-size: 4rem;
        font-weight: 800;

        @media (max-width: 800px) {
          font-size: 6vw;
        }
      }

      .prosperism-definition {
        max-width: 1100px;
        margin: 0 auto;

        img {
          width: 100%;
        }

        @media (max-width: 800px) {
          max-width: 1100px;
          margin: 0 auto;
        }
      }
    }
  }

  .transition {
    height: 70px;

    &.journal-bg {
      position: relative;
      margin-top: -165px;
    }

    @media (max-width: 800px) {
      height: 30px;
    }
  }

  .prosperist-journal {
    height: 450px;
    background: linear-gradient(
      0deg,
      rgba(227, 197, 172, 1) 0%,
      rgba(255, 255, 255, 1) 20%,
      rgba(255, 255, 255, 1) 80%,
      rgba(240, 226, 215, 1) 100%
    );
    padding: 1rem 0;
    color: #0c353f;

    @media (max-width: 800px) {
      height: auto;
    }

    & > .flex {
      @media (max-width: 800px) {
        flex-direction: column;
        gap: 2rem;
      }
    }

    .container {
      @media (max-width: 800px) {
        max-width: 100%;
        padding: 2rem;
      }
    }

    .journal-text.flex {
      flex-direction: column;
    }

    .flex {
      justify-content: center;
      align-items: center;
    }

    .journal-logo,
    .journal-text {
      width: 50%;
    }

    .journal-logo {
      @media (max-width: 800px) {
        width: 75%;
        height: auto;
      }
    }

    .journal-logo img {
      width: 70%;
      height: auto;

      @media (max-width: 800px) {
        width: 100%;
        height: auto;
      }
    }

    .journal-text {
      font-size: 2vw;
      text-align: center;
      gap: 1rem;
      padding: 2rem;

      @media (max-width: 800px) {
        padding: 0;
        height: auto;
        width: 100%;
        font-size: 4.5vw;
      }

      p {
        font-style: italic;
        line-height: 1;
        letter-spacing: 0vw;
      }

      .link {
        width: 100%;
        padding: 1rem 0;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;

        .svgIcon {
          height: 20px;
          width: auto;
        }

        &:hover .svgIcon {
          fill: #e1c1a7;
        }
      }
    }
  }

  .prosperist-projects {
    height: 600px;
    width: 100%;
    position: relative;
    color: #fff;
    font-size: 2rem;
    text-shadow: 0px 1px 5px rgba(0, 0, 0, 0.6);

    @media (max-width: 800px) {
      height: auto;
      text-align: center;
    }

    .container.flex {
      @media (max-width: 800px) {
        gap: 2rem;
        padding: 3rem;
      }
    }

    h1.journal-bg {
      padding: 1rem;

      @media (max-width: 800px) {
        font-size: 8vw;
      }
    }

    ul.flex {
      @media (max-width: 800px) {
        flex-direction: column;
        width: 100%;
        height: auto;
      }
    }

    ul li {
      @media (max-width: 800px) {
        max-width: none;
        width: 100%;
        height: auto;
        font-size: 7vw;
      }
    }

    li {
      text-shadow: 0px 1px 5px rgba(0, 0, 0, 0.6);
      max-width: 170px;
      text-align: center;
      line-height: 1.2;
      font-weight: 700;
      font-style: italic;
      padding: 0 0.5rem;
      cursor: initial;
    }

    &-bg {
      height: 100%;
      width: 100%;
      background: linear-gradient(
        90deg,
        rgba(0, 0, 0, 0.9) 0%,
        rgba(0, 66, 74, 0.9) 100%
      );
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
      display: flex;

      &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background-image: url("../assets/Images/table.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        background-position: bottom;
        z-index: -2;
      }

      & > .flex {
        flex-direction: column;
        height: 100%;
      }
    }

    .flex {
      justify-content: center;
      align-items: center;
      gap: 2rem;
      height: auto;
    }
  }

  .contact {
    height: 600px;
    width: 100%;
    position: relative;
    overflow: hidden;
    background: linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.9) 0%,
      rgba(74, 0, 37, 0.6) 100%
    );
    position: relative;

    @media (max-width: 800px) {
      height: auto;
      padding: 2rem 0;
    }

    &::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url("../assets/Images/library.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
      z-index: -3;
    }

    .flex {
      justify-content: center;
      align-items: center;
      gap: 2rem;

      @media (max-width: 800px) {
        flex-direction: column-reverse;
      }
    }

    .contact-form {
      width: 50%;

      &.flex {
        flex-direction: column;
        align-items: flex-end;
        gap: 1rem;
        padding: 0 2rem;

        @media (max-width: 800px) {
          width: 100%;
          height: auto;
          padding: 0 1rem;
        }
      }

      label {
        color: #fff;
        width: 100%;
        text-align: center;
        font-size: 5rem;
        line-height: 1;

        @media (max-width: 800px) {
          font-size: 2rem;
        }
      }

      textarea {
        resize: vertical;
      }

      input,
      button,
      textarea {
        width: 100%;
        height: 50px;
        border-radius: 10px;
        font-size: 1.5rem;
        background: none;
        border: none;
        color: #fff;

        @media (max-width: 800px) {
          font-size: 1.5rem;
        }
      }

      input {
        padding-left: 1rem;
        border-bottom: #fff 5px solid;
        box-shadow: 0px 5px 5px 2px rgba(0, 0, 0, 0.6);
        transition: 0.5s ease;

        &::placeholder {
          color: #fff;
          transition: 0.5s ease;
        }

        &:focus,
        &:focus-visible {
          outline: none;
          border-bottom: #e1c1a7 5px solid;

          &::placeholder {
            color: #e1c1a7;
          }
        }
      }

      textarea {
        padding-left: 1rem;
        border-bottom: #fff 5px solid;
        box-shadow: 0px 5px 5px 2px rgba(0, 0, 0, 0.6);
        transition: 0.5s ease;

        &::placeholder {
          color: #fff;
          transition: 0.5s ease;
        }

        &:focus,
        &:focus-visible {
          outline: none;
          border-bottom: #e1c1a7 5px solid;
        }

        &:focus {
          &::placeholder {
            color: #e1c1a7;
          }
        }

        &:focus-visible {
          &::placeholder {
            color: #e1c1a7;
          }
        }
      }

      button {
        border-bottom: #fff 5px solid;
        border-left: #fff 5px solid;
        border-right: #fff 5px solid;
        cursor: pointer;
        margin-top: 1rem;
        transition: 0.2s ease;

        &:hover {
          color: #e1c1a7;
          border-bottom: #e1c1a7 5px solid;
          border-left: #e1c1a7 5px solid;
          border-right: #e1c1a7 5px solid;
        }
      }
    }

    .contact-svg.flex {
      justify-content: flex-start;

      svg {
        height: 300px;
        width: auto;
        fill: #fff;
        transition: 1s fill ease;

        &:hover {
          fill: #e1c1a7;
        }

        @media (max-width: 800px) {
          width: 100%;
          max-height: 200px;
        }
      }

      @media (max-width: 800px) {
        width: 100%;
        height: auto;
        padding: 0 1rem;
      }
    }
  }
}
</style>
