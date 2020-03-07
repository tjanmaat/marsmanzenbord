<template>
  <div class="hello">
    <div class="par">
      <p>
        Dus jij denkt na op een lokale ronde naar de tweede plek te rijden
        <br>
        hier om de knikkers mee te kunnen strijden?
        <br>
        Voor een beetje fatsoenlijk vertoon
        <br>
        Met je eten liefst geblend,
        <br>
        twee benen met voor de profs te weinig talent
        <br>
        en een enorm bord voor je kop
        <br>
        bereik je hier niet zomaar de top.
      </p>
    </div>
    <h3>Regels</h3>
    <div class="par">
      <p>
        Ganzenbord, je kent het wel;
        <br>
        van begin naar eind en snel
        <br>
        Kom je op een getal te staan,
        <br>
        klik het dan hieronder aan.
      </p>
    </div>
    <ul>
      <li @click="$emit('numberClick', 1)"><a>1</a></li>
      <li @click="$emit('numberClick', 6)"><a>6</a></li>
      <li @click="$emit('numberClick', 9)"><a>9</a></li>
      <li @click="$emit('numberClick', 14)"><a>14</a></li>
      <li @click="$emit('numberClick', 16)"><a>16</a></li>
      <li @click="$emit('numberClick', 18)"><a>18</a></li>
      <li @click="$emit('numberClick', 22)"><a>22</a></li>
      <li @click="$emit('numberClick', 27)"><a>27</a></li>
      <li @click="$emit('numberClick', 32)"><a>32</a></li>
      <li @click="$emit('numberClick', 36)"><a>36</a></li>
      <li @click="$emit('numberClick', 40)"><a>40</a></li>
      <li @click="$emit('numberClick', 45)"><a>45</a></li>
      <li @click="$emit('numberClick', 50)"><a>50</a></li>
      <li @click="$emit('numberClick', 52)"><a>52</a></li>
      <li @click="$emit('numberClick', 58)"><a>58</a></li>
      <li @click="$emit('numberClick', 59)"><a>59</a></li>
      <li @click="$emit('numberClick', 61)"><a>61</a></li>
      <li @click="$emit('numberClick', 62)"><a>62</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 20px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

p {
  width: 100%;
  text-align: center;
}

.par {
  display: inline-block;
}
</style>
