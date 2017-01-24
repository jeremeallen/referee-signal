<template>
  <div id="app" class='container'>
    <div class='columns is-full'>
      <div class="tile is-ancestor">
        <div class="tile is-parent box" v-for='penalty in penalties'>
          <article class="tile is-child notification">
            <p class="title">{{ penalty.name }}</p>
            <p class="subtitle">With an image</p>
            <figure class="image penalties" :class="penalty.cssClass">
            </figure>
          </article>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      penalties: [
        {
          name: 'Boarding',
          description: 'When you board someone',
          cssClass: 'boarding',
        },
        {
          name: 'Butt-ending',
          description: 'When you butt end someone',
          cssClass: 'butt-ending',
        },
        {
          name: 'Charging',
          description: 'When you do the charging',
          cssClass: 'charging',
        },
        {
          name: 'Contact to the head',
          description: 'When you hit someone in the head',
          cssClass: 'head-contact',
        },
      ],
    };
  },
};
</script>
<style>
  .penalties {
    background-image: url('./assets/RefereePenaltysignals.png');
    background-repeat: no-repeat;
    width: 250px;
    height: 300px;
  }

  .boarding {
    background-position: -4px -10px;
  }

  .butt-ending {
    background-position: -220px -10px;
  }

  .charging {
    background-position: -440px -10px;
  }

  .head-contact {
    background-position: -660px -10px;
  }
</style>
