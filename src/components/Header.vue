<template>
    <div class="row">
          <div class="col-sm-12 col-md-12 col-lg-12">
              <h1>Quotes Added</h1>
      <div class="meter">
          <div class="quote-meter" role="progressbar" aria-valuenow="60" aria-valuemin="100"
          :style="{width: actualQuotes / maxQuotes * 100 + '%'}">{{actualQuotes}} / {{maxQuotes}}</div>
      </div>
  </div>
    </div>

</template>

<script>
export default {
    props: ['actualQuotes', 'maxQuotes'],
    data() {
        return {
            meter: this.meterMethod()
        }
    },
    methods: {
        meterMethod(){
            console.log(this.actualQuotes);
             return this.actualQuotes * 10;
        }
    },
}
</script>

<style>
    .meter{
        height:20px;
        max-width: 100%;
        background-color: lightgray;
        border-radius: 5px;
    }
    .quote-meter{
        height: 20px;

        background-color: lightcoral;
        border-radius: 5px;
        text-align: center;
        transition: width 1s ease;

        
    }
</style>