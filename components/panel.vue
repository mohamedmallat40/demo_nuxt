<template>
  <div class="container m-auto">
    <svg
      class="waves"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 1440 320"
      preserveAspectRatio="none"
    >
      <path
        fill="#fff"
        fill-opacity="1"
        d="M0,160L48,181.3C96,203,192,245,288,250.7C384,256,480,224,576,192C672,160,768,128,864,96C960,64,1056,32,1152,21.3C1248,11,1344,21,1392,26.7L1440,32L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
      ></path>
    </svg>
    <div id="mypanel" class="panel flex overflow-hidden ml-3 cursor-pointer">
      <div :style="{ left: leftBacgrkound }" class="background-x"></div>
      <div
        class="panel-elm panel-1 flex items-center justify-center flex-shrink-0 p-5"
        :class="{ selected: selected == 0 }"
        @click="change(0)"
      >
        <p class="text-center">Arbeitnehmer</p>
      </div>
      <div
        class="panel-elm flex items-center justify-center flex-shrink-0 p-5"
        :class="{ selected: selected == 1 }"
        @click="change(1)"
      >
        <p class="text-center">Arbeitgeber</p>
      </div>
      <div
        class="panel-elm flex items-center justify-center flex-shrink-0 panel-3 mr-4 p-5"
        :class="{ selected: selected == 2 }"
        @click="change(2)"
      >
        <p class="text-center">Temporärbüro</p>
      </div>
    </div>
    <Panelelm
      v-if="selected == 0"
      :h2="'Drei einfache Schritte zu deinem neuen Job'"
      :p1="'Erstellen dein Lebenslauf'"
      :p2="'Erstellen dein Lebenslauf'"
      :p3="'Mit nur einem Klick bewerben'"
      :img1="'undraw_Profile_data_re_v81r'"
      :img2="'imagep1-3'"
      :img3="'imagep1-2'"
      :end="true"
    />
    <Panelelm
      v-if="selected == 1"
      :h2="'Drei einfache Schritte zu deinem neuen Mitarbeiter'"
      :p1="'Erstellen dein Unternehmensprofil'"
      :p2="'Erstellen ein Jobinserat'"
      :p3="'Wähle deinen neuen Mitarbeiter aus'"
      :img1="'undraw_Profile_data_re_v81r'"
      :img2="'undraw_about_me_wa29'"
      :img3="'undraw_swipe_profiles1_i6mr'"
    />
    <Panelelm
      v-if="selected == 2"
      :h2="'Drei einfache Schritte zur Vermittlung neuer Mitarbeiter'"
      :p1="'Erstellen dein Unternehmensprofil'"
      :p2="'Erhalte Vermittlungs- angebot von Arbeitgeber'"
      :p3="'Vermittlung nach Provision oder Stundenlohn'"
      :img1="'undraw_Profile_data_re_v81r'"
      :img2="'undraw_job_offers_kw5d'"
      :img3="'undraw_business_deal_cpi9'"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: 0,
      leftBacgrkound: 1,
      panel: null,
    }
  },
  methods: {
    getScrollX(select, index) {
      if (index === 0) {
        return -160
      }
      if (select > index) {
        return (-index * 160) / 2
      }

      return (index * 160) / 2
    },
    change(index) {
      this.panel = document.getElementById('mypanel')
      this.panel.scrollBy(this.getScrollX(this.selected, index), 0)
      this.selected = index
      if (index >= 0) {
        this.leftBacgrkound = index * 160 + 'px'
      }
    },
  },
}
</script>

<style>
.background-x {
  position: absolute;
  width: 160px;
  height: 100%;
  background-color: #81e6d9;
  transition: all 0.3s;
}
.panel {
  position: relative;
  border-radius: 12px 0px 0px 12px;
  scroll-behavior: smooth;
  transition: all 0.3s;
}
.panel-elm {
  border: 1px solid #cbd5e0;
  width: 160px;
  height: 40px;
  color: #319795;
}
.panel-elm:hover {
  background: #81e6d954;
}

.panel-elm p {
  text-align: center;
  font-weight: bold;
  font-size: 17px;
  z-index: 4;
  letter-spacing: 0.84px;
}
.panel-1 {
  border-radius: 12px 0px 0px 12px;
}
.panel-3 {
  border-radius: 0px 12px 12px 0px;
}
.selected {
  /* background: #81e6d9; */
  color: white;
  transition: all 0.3s;
}
.waves {
  height: 7rem;
  width: 100%;
  margin-top: -6rem;
}
@media (min-width: 700px) {
  .panel {
    /* justify-content: center;
    width: 100%; */
    margin: 3rem auto;
    width: max-content;
  }
  .waves {
    display: none;
  }
  .w-screen {
    width: 99vw !important;
  }
}
</style>
