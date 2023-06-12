<template>
  <div>
    <img src="https://phoneky.co.uk/thumbs/screensavers/down/misc/dancinghea063213.gif" class="right-image">
    <img src="https://imagensemoldes.com.br/wp-content/uploads/2023/02/Flork-Coracao-Partido-PNG.png" class="left-image2">
    <div class="body_column">
      <h1><v-icon>mdi-heart</v-icon>Você aceita casar comigo?<v-icon>mdi-heart</v-icon></h1>
      <div class="yes-or-no button_row">
        <v-button class="yes" @click="acceptProposal">SIM<v-icon>mdi-heart</v-icon></v-button>
        <v-button class="no">NÃO!</v-button>
      </div>
    </div>
    <v-footer :absolute="!fixed" app>
      <span>&copy; caetano leal {{ new Date().getFullYear() }}</span>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fixed: false
    };
  },
  methods: {
    acceptProposal() {
      this.$router.push('/sim');
    },
  },
  mounted() {
    let btn = document.querySelector(".no");
    let position = 0;
    if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
      btn.addEventListener("touchstart", function() {
        position ? (position = 0) : (position = 150);
        btn.style.transform = `translate(${position}px,0px)`;
        btn.style.transition = "all 0.3s ease";
      });

      btn.addEventListener("touchend", function() {
        position ? (position = 0) : (position = 150);
        btn.style.transform = `translate(${position}px,0px)`;
        btn.style.transition = "all 0.3s ease";
      });
    } else {
      btn.addEventListener("mouseover", function() {
        position ? (position = 0) : (position = 300);
        btn.style.transform = `translate(${position}px,0px)`;
        btn.style.transition = "all 0.2s ease";
      });
    }
  }
};
</script>

<style>
.body_column {
  margin: 0;
  padding: 0;
  background: rgb(222, 131, 214);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100vh;
  font-family: Arial, Helvetica, sans-serif;
}
.button_row {
  display:flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
}

.yes-or-no {
  height: 120px;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50%;
}

.yes-or-no .yes {
  font-weight: bold;
  margin-right: 30px;
  background: rgb(132, 207, 132);
  color: white;
  font-size: 2rem;
  border-radius: 8px;
  padding: 15px;
  text-transform: uppercase;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.5);
}

.yes-or-no .no {
  margin-left: 30px;
  font-weight: bold;
  background: rgb(255, 3, 3);
  color: white;
  font-size: 2rem;
  border-radius: 8px;
  padding: 15px;
  text-transform: uppercase;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.5);
}

h1 {
  color: #fff;
  display: block;
  font-size: 3em;
  margin-block-start: 0.67em;
  margin-block-end: 0.67em;
  margin-inline-start: 10%;
  margin-inline-end: 10%;
  font-weight: bold;
}
.right-image {
  position: absolute;
  right: 0;
  top: 0;
}
.left-image2 {
  position: absolute;
  left: 0;
  top: 420px;
  width: 280px;
}
</style>
