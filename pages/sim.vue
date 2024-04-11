<template>
  <div>
    <body class="body_column">
      <h1><v-icon>mdi-heart</v-icon>indo comer seu cu<v-icon>mdi-heart</v-icon></h1>
      <div>
          <img src="https://i.gifer.com/F8Hc.gif" class="coracao-andando">
      </div>
    </body>
  </div>
</template>

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
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.5)
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
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.5)
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
.coracao-andando{
  height: 320px;
  width: 420px
}
</style>