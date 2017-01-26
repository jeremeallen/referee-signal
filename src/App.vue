<template>
  <div id="app" class='container-fluid'>
    <div class='row'>
      <div class="col-xs-12 col-sm-4 col-md-3" v-for='penalty in penalties'>
        <div class="panel panel-default">
          <div class="panel-heading">
            <h3 class="text-center">{{ penalty.name }}</h3>
          </div>
          <div class="panel-body">
            <div class="image penalties" :class="penalty.cssClass"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import penalties from './data';

export default {
  name: 'app',
  data() {
    return penalties;
  },
};
</script>
<style>
  .penalties {
    background-image: url('./assets/RefereePenaltysignals.png');
    background-repeat: no-repeat;
    width: 210px;
    height: 240px;
    margin: 0 auto;
  }

  .boarding {
    background-position: -4px -10px;
  }

  .butt-ending {
    background-position: -240px -10px;
  }

  .charging {
    background-position: -470px -10px;
  }

  .head-contact {
    background-position: -720px -15px;
  }

  .cross-checking {
    background-position: -940px -10px;
  }

  .delayed-call {
    background-position: -1160px -10px;
  }

  .delayed-game {
    background-position: -5px -320px;
  }

  .elbowing {
    background-position: -220px -320px;
  }

  .roughing {
    background-position: -480px -320px;
  }

  .hand-pass {
    background-position: -710px -320px;
  }

  .high-sticking {
    background-position: -940px -320px;
  }

  .hitting-behind {
    background-position: -1160px -320px;
  }

  .holding {
    background-position: -5px -630px;
  }

  .holding-stick {
    background-position: -240px -630px;
  }

  .hooking {
    background-position: -710px -630px;
  }

  .icing {
    background-position: -940px -630px;
  }

  .unsportsmanlike {
    background-position: -1160px -630px;
  }

  .tripping {
    background-position: -110px -940px;
  }

  .kneeing {
    background-position: -360px -940px;
  }

  .misconduct {
    background-position: -580px -940px;
  }

  .spearing {
    background-position: -810px -940px;
  }

  .slashing {
    background-position: -1050px -940px;
  }

  @media only screen and (min-width : 320px) {
    h3 {
      font-size: 20px
    }
  }

  /* Extra Small Devices, Phones */
  @media only screen and (min-width : 480px) {
    h3 {
      font-size: 24px
    }
  }

  /* Small Devices, Tablets */
  @media only screen and (min-width : 768px) {
    h3 {
      font-size: 20px
    }
  }

  /* Medium Devices, Desktops */
  @media only screen and (min-width : 992px) {
    h3 {
      font-size: 16px
    }
  }

  /* Large Devices, Wide Screens */
  @media only screen and (min-width : 1200px) {
    h3 {
      font-size: 24px
    }
  }
</style>
