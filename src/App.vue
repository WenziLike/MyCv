<template>
  <div class="container">
    <div class="wrapper">
      <div class="wrapper-social">
        <ul>
          <li>
            <a href="#" class="">facebook</a>
          </li>
          <li>
            <a href="#">Telegram</a>
          </li>
          <li>
            <a href="#">Git</a>
          </li>
        </ul>
      </div>
      <div class="wrapper-content">
        <div class="wrapper-logo"><strong>VM</strong></div>
        <h1 class="wrapper-title">Viacheslav Murakhin</h1>
        <div class="wapper-content flex-sa">
          <div class="card">
            <div class="card shadow-drop-2-center">
              <div class="card circle-image"></div>
              <ul>
                <li>
                  <strong>tel:</strong>
                  <a href="tel:+48537886161"
                    ><strong> +48 537 88 61 61</strong>
                  </a>
                </li>
                <li>
                  <strong>email:</strong>
                  <a href="mailto:SlavaMyraxin@icloud.com"
                    ><strong> SlavaMyraxin@icloud.com</strong>
                  </a>
                </li>
                <li>
                  <strong>Skype:</strong>
                  <a href="callto:skype:live:.cid.f00786ab772de349"
                    ><strong> Skype</strong>
                  </a>
                </li>
              </ul>
              <div class="card-adress">
                <p>31-425 Kraków, Poland</p>
                <p>Rogatka 7</p>
              </div>
            </div>
            <div class="skills">
              <h2>Skills</h2>
              <ul>
                <li>
                  <a href="https://html.spec.whatwg.org" target="_blank"
                    >HTML</a
                  >
                </li>
                <li>
                  <a href="https://www.w3.org/Style/CSS/" target="_blank"
                    >CSS</a
                  >
                </li>
                <li>
                  <a href="https://sass-lang.com/" target="_blank">SCSS/SASS</a>
                </li>
                <li>
                  <a
                    href="https://en.wikipedia.org/wiki/JavaScript"
                    target="_blank"
                    >Java Script</a
                  >
                </li>
                <li>
                  <a href="https://v3.vuejs.org" target="_blank">Vue v2/3</a>
                </li>
                <li>
                  <a
                    href="https://v3.vuejs.org/api/composition-api.html#setup"
                    target="_blank"
                    >Composition Api</a
                  >
                </li>
                <li>
                  <a href="https://next.vuex.vuejs.org" target="_blank">VueX</a>
                </li>
                <li>
                  <a href="https://next.router.vuejs.org" target="_blank"
                    >Router</a
                  >
                </li>
                <li>
                  <a href="https://www.npmjs.com" target="_blank">NPM</a>
                </li>
                <li><a href="https://github.com" target="_blank">Git</a></li>
                <li>
                  <a href="https://firebase.google.com" target="_blank"
                    >FireBase</a
                  >
                </li>
                <li>
                  <a
                    href="https://analytics.google.com/analytics"
                    target="_blank"
                    >Google Web Analytics</a
                  >
                </li>
                <li>
                  <a
                    href="https://www.adobe.com/products/photoshop.html"
                    target="_blank"
                    >Photoshop</a
                  >
                </li>
              </ul>
              <h4 class="skills-sub-title">Transpilator :</h4>
              <hr />
              <ul>
                <li>
                  <a href="https://webpack.js.org" target="_blank">WebPack</a>
                </li>
                <li><a href="https://gulpjs.com" target="_blank">Gulp</a></li>
              </ul>
            </div>
            <div class="br-3">
              <h2>info</h2>
            </div>
            <div class="br-3">
              <h2>Dev</h2>
            </div>
          </div>

          <div class="card flex-auto br-3 m-2">
            <h2>Vue 3</h2>
            <div class="text">
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Laboriosam alias perferendis nemo quaerat a laudantium ut vero
                animi quibusdam distinctio rem quo harum nulla, sit deleniti
                ullam quae soluta culpa!
              </p>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Laboriosam alias perferendis nemo quaerat a laudantium ut vero
                animi quibusdam distinctio rem quo harum nulla, sit deleniti
                ullam quae soluta culpa!
              </p>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Laboriosam alias perferendis nemo quaerat a laudantium ut vero
                animi quibusdam distinctio rem quo harum nulla, sit deleniti
                ullam quae soluta culpa!
              </p>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Laboriosam alias perferendis nemo quaerat a laudantium ut vero
                animi quibusdam distinctio rem quo harum nulla, sit deleniti
                ullam quae soluta culpa!
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 4%;
  .wrapper {
    position: relative;
    &-social {
      position: fixed;
      top: 2%;
      right: 6%;
      z-index: -1;
      ul {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        li {
          margin-right: 9%;
          a {
            font-weight: 700;
            font-size: 1.1em;
            background: linear-gradient(
              45deg,
              #0b2349 33%,
              #0d61bc 66%,
              #8aa9d6
            );
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            &:hover {
              background: linear-gradient(
                18deg,
                #000000 33%,
                #18ca00 66%,
                #8aa9d6
              );
              -webkit-background-clip: text;
              -webkit-text-fill-color: transparent;
            }
          }
        }
      }
    }
    &-logo {
      position: absolute;
      left: 2%;
      top: 4%;
    }
    &-title {
      position: relative;
      text-align: center;
      top: 50px;
      left: 20px;
    }
    &-content {
      background-color: #eef2f3;
      .m-2 {
        margin-right: 0;
      }
      .card {
        .shadow-drop-2-center {
          text-align: center;
        }
        a {
          color: #2c3e50;
        }
        &-adress {
          font-weight: 700;
          font-style: italic;
          p {
            margin: 0;
            &:nth-child(1) {
              margin-top: 18px;
            }
          }
        }
      }
      .skills {
        hr {
          margin-top: 0;
        }
        &-sub-title {
          margin-bottom: 0;
        }
        & li {
          line-height: 1.7;
          cursor: pointer;
          &:hover {
            a {
              font-weight: 700;
              font-style: italic;
              font-size: 1.5em;
              background: linear-gradient(
                45deg,
                #0b2349 33%,
                #0d61bc 66%,
                #8aa9d6
              );
              -webkit-background-clip: text;
              -webkit-text-fill-color: transparent;
            }
            border-bottom: 2px solid rgb(5, 147, 212);
          }
        }
      }
    }
  }

  .text {
    font-size: 18px;
    font-weight: 500;
  }
}
</style>
