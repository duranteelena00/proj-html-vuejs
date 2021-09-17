<template>
  <div class="content">
    <Main />
    <section id="business-news">
      <div class="container">
        <div class="text pb-4">
          <h4>OUR EDITORIAL CONTENT</h4>
          <h2 class="py-4">Latest <span class="turquoise px-2">News</span></h2>
          <p>
            Every week we publish content about what is best in the business
            world.
          </p>
        </div>
        <div class="row">
          <div class="col" v-for="(article, index) in news" :key="index">
            <div class="card py-5">
              <p class="border border-primary">
                <span class="pe-2"
                  ><i class="far fa-user pe-1"></i>{{ article.author }}</span
                >
                <span class="ps-2"
                  ><i class="far fa-clock pe-1"></i>{{ article.date }}</span
                >
              </p>
              <img :src="article.imgUrl" alt="" />
              <h3>{{ article.title }}</h3>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="newsletter">
      <img src="@/assets/img/bg-1.jpg" alt="" />
      <div class="container d-flex">
        <div class="text pb-5">
          <h4>NEWSLETTER</h4>
          <h2 class="py-4">Know<span class="turquoise px-2">First</span></h2>
          <p>
            Follow closely and receive content about our company and the news of
            the current market.
          </p>
        </div>
        <div class="form d-flex flex-column">
          <input type="text" placeholder="Name" /><input
            type="text"
            placeholder="email"
          /><button type="button" class="turquoise mt-3">Subscribe</button>
        </div>
      </div>
    </section>
    <section id="contact-the-company">
      <div class="container d-flex flex-row">
        <div class="form pe-3">
          <div class="text pb-4">
            <h4>SEND A MESSAGE</h4>
            <h2 class="py-4">Get in<span>Touch</span></h2>
            <p>We will respond to your message as soon as possible.</p>
          </div>
          <div class="row">
            <div class="col d-flex align-items-center">
              <input type="text" name="" id="" placeholder="Name" /><span
                ><i class="fas fa-file-download"></i
              ></span>
            </div>
            <div class="col">
              <input type="text" name="" id="" placeholder="Email" />
            </div>
          </div>
          <div class="row">
            <div class="col">
              <input type="number" name="" id="" placeholder="Phone" />
            </div>
            <div class="col d-flex align-items-center">
              <input type="text" placeholder="More Info" />
              <span><i class="fas fa-angle-down"></i></span>
            </div>
          </div>
          <input type="textarea" placeholder="message" />
          <button type="button" class="turquoise mt-3">Send</button>
        </div>
        <div id="contacts" class="ps-5">
          <h3 class="my-3">Example Inc.</h3>
          <p class="pb-2">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
          </p>
          <p class="pb-4">Delectus quas et sed sit doloremque temporibus!</p>
          <ul>
            <li class="pb-2">
              <i class="fas fa-phone-alt me-2"></i>{{ contacts.number }}
            </li>
            <li class="pb-2">
              <i class="fas fa-envelope me-2"></i>{{ contacts.email }}
            </li>
            <li>
              <i class="fas fa-map-marker-alt me-2"></i>{{ contacts.office }}
            </li>
            <li class="pb-2">
              <button type="button" class="transparent mt-3">VIEW MAP</button>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Main from "@/components/Main.vue";

export default {
  name: "Content",
  components: { Main },
  props: {
    contacts: Object,
    links: Array,
  },
  data() {
    return {
      news: [
        {
          imgUrl: require("@/assets/img/news-1.jpg"),
          title: "Increasing creativity is possible for everyone",
          author: "Andrea Miller",
          date: "2 Days Ago",
        },
        {
          imgUrl: require("@/assets/img/news-2.jpg"),
          title: "Becouse market research is part of the business plan",
          author: "Tiffany Gaines",
          date: "Today",
        },
        {
          imgUrl: require("@/assets/img/news-3.jpg"),
          title: "Work from home is now a trend",
          author: "Lia Walsh",
          date: "9-08-2021",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
p {
  color: rgb(148, 147, 147);
}

#business-news {
  .container {
    flex-direction: column;
  }
  .row > .col > .card {
    background: black;
    position: relative;
    border-radius: 5px;
    min-height: 250px;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      border-radius: 5px;
      opacity: 0.5;
      position: absolute;
      top: 0;
      left: 0;
    }
    p {
      position: absolute;
      top: 0;
    }
    h3 {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
    }
    i {
      color: rgb(148, 147, 147);
    }
  }
}

#newsletter {
  position: relative;
  color: rgb(148, 147, 147);
  img {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    object-fit: cover;
    object-position: center;
    z-index: -1;
  }
}

#newsletter .text {
  flex-grow: 1;
}

#newsletter .text > h2 {
  color: white;
}
#newsletter .text > h2 > span.turquoise {
  color: white;
  background: rgb(30, 67, 73);
}

#newsletter input {
  background: rgb(179, 189, 192);
  margin: 5px 0;
  border-radius: 5px;
  width: 100%;
}

#newsletter button {
  width: 50%;
}

#newsletter .form {
  width: 27.5%;
}

#contact-the-company > .container {
  flex-direction: row;
}

#contact-the-company .form {
  flex-grow: 1;
}

#contact-the-company input {
  background: rgb(236, 236, 236);
  margin: 5px 0;
  width: 100%;
}

#contact-the-company .form i {
  color: grey;
  background: rgb(236, 236, 236);
  padding: 9.65px;
}

#contact-the-company #contacts {
  width: 45%;
  i {
    margin: 0;
    padding: 12.5px;
    color: teal;
    font-size: 15px;
    border-radius: 50%;
    background: rgb(218, 236, 237);
  }
  button {
    color: #038483;
  }
}
</style>