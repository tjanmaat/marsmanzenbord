<template>
  <div class="modal-mask" @click="$emit('close')">
    <div class="modal-wrapper">
      <div class="modal-container">

        <div class="modal-header">
          <slot name="header">
            <b>
              {{getHeader()}}
            </b>
          </slot>
        </div>

        <div class="modal-body">
          <slot name="body">
            <i>
              {{getRhyme(1)}}
              <br>
              {{getRhyme(2)}}
              <br>
              {{getRhyme(3)}}
              <br>
              {{getRhyme(4)}}
            </i>
          </slot>
        </div>

        <div class="modal-footer">
          <slot name="footer">
            {{getResult()}}
          </slot>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NumberModal',
  props: {
    clickedNumber: null,
    isDrinkGame: null
  },
  methods:{
    getHeader(){
      if (this.clickedNumber === 1){
        return "Papierwerk"
      } else if (this.clickedNumber === 6){
        return "Overmoedig"
      } else if (this.clickedNumber === 9){
        return "Blokkade"
      } else if (this.clickedNumber === 14){
        return "Pillen"
      } else if (this.clickedNumber === 16){
        return "Draaidop"
      } else if (this.clickedNumber === 18){
        return "Zingend"
      } else if (this.clickedNumber === 22){
        return "Zeven sloten"
      } else if (this.clickedNumber === 27){
        return "Wildkamperen"
      } else if (this.clickedNumber === 32){
        return "Nuchter"
      } else if (this.clickedNumber === 36){
        return "Man zonder plan"
      } else if (this.clickedNumber === 40){
        return "Op goed geluk"
      } else if (this.clickedNumber === 45){
        return "Zonnesteek"
      } else if (this.clickedNumber === 50){
        return "Kiezels"
      } else if (this.clickedNumber === 52){
        return "Kink"
      } else if (this.clickedNumber === 58){
        return "Siesta"
      } else if (this.clickedNumber === 59){
        return "Spoorloos"
      } else if (this.clickedNumber === 61){
        return "Glas"
      } else if (this.clickedNumber === 62){
        return "Score bord"
      } else {
        return "Dat is gek, hier hoor je niet te komen."
      }
    },
    getRhyme(line_number){
      if (this.clickedNumber === 1){
        if (line_number === 1){
          return "Maanden vorm smeden,"
        } else if (line_number === 2) {
          return "dagen gepland en"
        } else if (line_number === 3) {
          return "zelf goed warmgereden,"
        } else if (line_number === 4) {
          return "maar niet de juiste documenten."
        }
      } else if (this.clickedNumber === 6){
        if (line_number === 1){
          return "Noem het tactiek,"
        } else if (line_number === 2) {
          return "noem het overmoed,"
        } else if (line_number === 3) {
          return "dom of fanatiek,"
        } else if (line_number === 4) {
          return "de harde start gaat tot nu toe goed."
        }
      } else if (this.clickedNumber === 9){
        if (line_number === 1){
          return "Route tot in detail uitgezocht"
        } else if (line_number === 2) {
          return "dagen aan streetview verknocht,"
        } else if (line_number === 3) {
          return "dus dan is dit gewoon pech"
        } else if (line_number === 4) {
          return "gesloten hek op de weg."
        }
      } else if (this.clickedNumber === 14){
        if (line_number === 1){
          return "Caffëinepillen op zak,"
        } else if (line_number === 2) {
          return "maar vannacht geen zin daarin."
        } else if (line_number === 3) {
          return "Na een paar bermdutjes nog steeds brak"
        } else if (line_number === 4) {
          return "toch maar een hotel in."
        }
      } else if (this.clickedNumber === 16){
        if (line_number === 1){
          return "Tweede avond het is al laat."
        } else if (line_number === 2) {
          return "Helaas je waterzak niet goed gedicht."
        } else if (line_number === 3) {
          return "Gelukkig scheelt dat wel gewicht"
        } else if (line_number === 4) {
          return "als je zo de Stelvio op gaat."
        }
      } else if (this.clickedNumber === 18){
        if (line_number === 1){
          return "'s Nachts de Stelvio afrollen"
        } else if (line_number === 2) {
          return "is een enorm slecht idee."
        } else if (line_number === 3) {
          return "Op de fiets zingen, toch knikkebollen;"
        } else if (line_number === 4) {
          return "eerste hotel in daar benee."
        }
      } else if (this.clickedNumber === 22){
        if (line_number === 1){
          return "Een hittegolf in europa."
        } else if (line_number === 2) {
          return "Het kwik stijft tot 42 graden."
        } else if (line_number === 3) {
          return "Fietsen kan hierna,"
        } else if (line_number === 4) {
          return "eerst in een beekje baden."
        }
      } else if (this.clickedNumber === 27){
        if (line_number === 1){
          return "Geplande nacht onderaan de finestre, waar"
        } else if (line_number === 2) {
          return "helemaal geen hotel blijkt te zijn"
        } else if (line_number === 3) {
          return "Slapen in de berm is naar,"
        } else if (line_number === 4) {
          return "maar zonder eten doet nog meer pijn."
        }
      } else if (this.clickedNumber === 32){
        if (line_number === 1){
          return "Uit de Stelvio trok je een les"
        } else if (line_number === 2) {
          return "klimmen zonder water was een groot succes."
        } else if (line_number === 3) {
          return "Op de finestre dus de overtreffende trap;"
        } else if (line_number === 4) {
          return "wat als ik ook het eten schrap?"
        }
      } else if (this.clickedNumber === 36){
        if (line_number === 1){
          return "Al een etmaal op het schema achter"
        } else if (line_number === 2) {
          return "houd het schema opeens op."
        } else if (line_number === 3) {
          return "Zonder fiets je een stuk zachter,"
        } else if (line_number === 4) {
          return "raak je nog meer achterop."
        }
      } else if (this.clickedNumber === 40){
        if (line_number === 1){
          return "Je blijkt een eind van de route te rijden."
        } else if (line_number === 2) {
          return "Gelukkig ligt daar al Avignon"
        } else if (line_number === 3) {
          return "en zag niemand dat het veel korter kon"
        } else if (line_number === 4) {
          return "Je kan zelfs om plek drie meestrijden."
        }
      } else if (this.clickedNumber === 45){
        if (line_number === 1){
          return "De zon is nog feller dan twee dagen terug"
        } else if (line_number === 2) {
          return "daar is niet tegenop te smeren,"
        } else if (line_number === 3) {
          return "maar zonder bescherming van kleren"
        } else if (line_number === 4) {
          return "verbrand je sowieso je hele rug."
        }
      } else if (this.clickedNumber === 50){
        if (line_number === 1){
          return "Strak langs de zee"
        } else if (line_number === 2) {
          return "valt de afstand en hoogte mee,"
        } else if (line_number === 3) {
          return "maar het wegdek helaas tegen"
        } else if (line_number === 4) {
          return "je rijd over grindpaden, geen wegen."
        }
      } else if (this.clickedNumber === 52){
        if (line_number === 1){
          return "Gezwind naar Perpignan."
        } else if (line_number === 2) {
          return "Over grind fietst nooit leuk"
        } else if (line_number === 3) {
          return "maar een kabelbreuk"
        } else if (line_number === 4) {
          return "maakt dat je helemaal moeilijk vooruit kan."
        }
      } else if (this.clickedNumber === 58){
        if (line_number === 1){
          return "In Perpignan aangekomen"
        } else if (line_number === 2) {
          return "zal de fietsenmaker gesloten blijken."
        } else if (line_number === 3) {
          return "Heet een paar uur lunchpauze genomen,"
        } else if (line_number === 4) {
          return "kan jij mooi even tour kijken."
        }
      } else if (this.clickedNumber === 59){
        if (line_number === 1){
          return "Je GPS-tracker valt uit,"
        } else if (line_number === 2) {
          return "dus online kom je niet meer vooruit."
        } else if (line_number === 3) {
          return "Dat heeft niet veel gevolgen,"
        } else if (line_number === 4) {
          return "maar is jammer voor hen die volgen."
        }
      } else if (this.clickedNumber === 61){
        if (line_number === 1){
          return "Geen kans meer op een mooie plek."
        } else if (line_number === 2) {
          return "Je laatste binnenbanden lek"
        } else if (line_number === 3) {
          return "en een scheur in je buitenband"
        } else if (line_number === 4) {
          return "zorgen dat je vlak voor Barcelona strand."
        }
      } else if (this.clickedNumber === 62){
        if (line_number === 1){
          return "Je nadert het eind op plek acht,"
        } else if (line_number === 2) {
          return "niet bepaald van voren,"
        } else if (line_number === 3) {
          return "niet bepaald onverwacht;"
        } else if (line_number === 4) {
          return "weer verloren."
        }
      } else {
        return "hoi"
      }
    },
    getResult(){
      if (this.clickedNumber === 1){
        if (this.isDrinkGame){
          return 'Ga je een beurt schamen. Probeer vooral je schaamte weg te spoelen met drie slokken.'
        } else {
          return 'Ga je een beurt schamen.'
        }
      } else if (this.clickedNumber === 6){
        if (this.isDrinkGame){
          return 'Gooi de dobbelsteen, voor ieder oog mag je een stap vooruit en een slok nemen.'
        } else {
          return 'Gooi de dobbelsteen, voor ieder oog mag je een stap vooruit.'
        }
      } else if (this.clickedNumber === 9){
        if (this.isDrinkGame){
          return 'Doe een stap terug om een nieuwe route te vinden. Neem onderweg gelijk een slok.'
        } else {
          return 'Doe een stap terug om een nieuwe route te vinden.'
        }
      } else if (this.clickedNumber === 14){
        if (this.isDrinkGame){
          return 'Neem twee slokken, doe twee stappen vooruit en pak een beurt goede nachtrust.'
        } else {
          return 'Doe twee stappen vooruit en pak een beurt goede nachtrust.'
        }
      } else if (this.clickedNumber === 16){
        if (this.isDrinkGame){
          return 'Drink snel je bidon leeg voor er niets meer over is en ga twee stappen terug.'
        } else {
          return 'Ga twee stappen terug.'
        }
      } else if (this.clickedNumber === 18){
        if (this.isDrinkGame){
          return 'Neem drie slokken om van de schrik te bekomen en ga een beurt slapen.'
        } else {
          return 'Ga een beurt slapen.'
        }
      } else if (this.clickedNumber === 22){
        if (this.isDrinkGame){
          return 'Neem een slok van de beek en doe een stap terug.'
        } else {
          return 'Doe een stap terug.'
        }
      } else if (this.clickedNumber === 27){
        if (this.isDrinkGame){
          return 'Vul je maag met je laatst water en ga een beurt slapen.'
        } else {
          return 'Ga een beurt slapen.'
        }
      } else if (this.clickedNumber === 32){
        if (this.isDrinkGame){
          return 'Ga drie stappen terug om te kijken of daar nou iets te eten lag.'
        } else {
          return 'Ga drie stappen terug om te kijken of daar nou iets te eten lag.'
        }
      } else if (this.clickedNumber === 36){
        if (this.isDrinkGame){
          return 'Neem twee slokken om nieuwe moed in te drinken en ga een stap terug.'
        } else {
          return 'Ga een stap terug.'
        }
      } else if (this.clickedNumber === 40){
        if (this.isDrinkGame){
          return 'Ga een stap vooruit en neem een slok.'
        } else {
          return 'Ga een stap vooruit.'
        }
      } else if (this.clickedNumber === 45){
        if (this.isDrinkGame){
          return 'Vooral nu is hydrateren belangrijk. Leeg je bidon en ga twee stappen terug.'
        } else {
          return 'Ga twee stappen terug.'
        }
      } else if (this.clickedNumber === 50){
        if (this.isDrinkGame){
          return 'Neem een slok om spoeler over het grind te rijden en ga een stap terug.'
        } else {
          return 'Ga een stap terug.'
        }
      } else if (this.clickedNumber === 52){
        if (this.isDrinkGame){
          return 'Sla een beurt over en neem twee slokken.'
        } else {
          return 'Sla een beurt over.'
        }
      } else if (this.clickedNumber === 58){
        if (this.isDrinkGame){
          return 'Sla een beurt over en gebruik die tijd om je bidon te legen.'
        } else {
          return 'Sla een beurt over.'
        }
      } else if (this.clickedNumber === 59){
        if (this.isDrinkGame){
          return 'Ga een stao vooruit en neem vier slokken.'
        } else {
          return 'Ga een stao vooruit.'
        }
      } else if (this.clickedNumber === 61){
        if (this.isDrinkGame){
          return 'Wacht tot een andere speler je inhaalt om je een bandje te geven. Drink iedere beurt een bidon leeg.'
        } else {
          return 'Wacht tot een andere speler je inhaalt om je een bandje te geven.'
        }
      } else if (this.clickedNumber === 62){
        if (this.isDrinkGame){
          return 'Drink je bidon leeg om de moed te vinden je ouders onder ogen te komen en doe twee stappen terug..'
        } else {
          return 'Doe twee stappen terug.'
        }
      } else {
        return "Dit is niet waar je wilt zijn."
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: table;
    transition: opacity 0.3s ease;
  }

  .modal-wrapper {
    display: table-cell;
    vertical-align: middle;
  }

  .modal-container {
    width: 350px;
    height: 180px;
    margin: 0 auto;
    padding: 20px 30px;
    background-color: #fff;
    border-radius: 2px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
    transition: all 0.3s ease;
    font-family: Helvetica, Arial, sans-serif;
  }

  .modal-header h3 {
    margin-top: 0;
    color: #42b983;
  }

  .modal-body {
    margin: 20px 0;
  }

  .modal-enter .modal-container,
  .modal-leave-active .modal-container {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
</style>
