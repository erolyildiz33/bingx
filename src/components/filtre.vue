<template>
    <div>
      <input type="radio" class="btn-check" name="options-outlined" id="all" autocomplete="off" checked>
      <label class="btn btn-outline-info rounded-pill mx-2" for="all">Hepsi</label>

      <input type="radio" class="btn-check" name="options-outlined" id="sifir" autocomplete="off">
      <label class="btn btn-outline-info rounded-pill mx-2" for="sifir">BingX Vadeli İşlemler</label>

      <input type="radio" class="btn-check" name="options-outlined" id="iki" autocomplete="off">
      <label class="btn btn-outline-info rounded-pill mx-2" for="iki">BingX Sürekli Vadeli</label>

      <input type="radio" class="btn-check" name="options-outlined" id="bir" autocomplete="off">
      <label class="btn btn-outline-info rounded-pill mx-2" for="bir">Binance Vadeli İşlemler</label>
  
      <div class="mb-3">
        <label ><span class="float-start" >Kümülatif PnL (USDT)</span ><span class="float-end"> {{kumulatif_pnl}}-2000+</span></label>
        <Slider  class="slider-blue"  v-model="kumulatif_pnl" :step="200" :min="0" :max="2000"  :tooltips="false" />
     </div>
  
     <div class="mb-3">
        <label class="form-label"> <span class="float-start" >Hesap Varlıkları (USDT)</span ><span class="float-end"> {{hesap_varliklari}}-10000+</span></label>
        <Slider  class="slider-blue"  v-model="hesap_varliklari" :step="1000" :min="0" :max="10000"  :tooltips="false"  />
      </div>

        <div class="mb-3">
          <label class="form-label"><span class="float-start" >Takipçiler</span ><span class="float-end"> {{takipciler}}-3000+</span></label>
          <Slider  class="slider-blue"  v-model="takipciler" :step="300" :min="0" :max="3000"  :tooltips="false"/>
       </div>
       <div class="mb-3">
          <label  class="form-label"><span class="float-start" >Kümülatif Kazançlar (USDT)</span ><span class="float-end"> {{kumulatif_kazanc}}-10000+</span></label>
          <Slider  class="slider-blue"  v-model="kumulatif_kazanc" :step="1000" :min="0" :max="10000"  :tooltips="false"/>
       </div>
       <div class="mb-3">
          <label  class="form-label"><span class="float-start" >30G ROI</span ><span class="float-end"> {{roi}}-200%+</span></label>
          <Slider  class="slider-blue"  v-model="roi" :step="20" :min="0" :max="200"  :tooltips="false"/>
       </div>
       <div class="mb-3">
          <label  class="form-label"><span class="float-start" >Risk</span ><span class="float-end"> {{risk}}-9</span></label>
          <Slider  class="slider-blue"  v-model="risk" :step="1" :min="0" :max="9"  :tooltips="false"/>
       </div>
       <div class="mb-3">
          <label  class="form-label"><span class="float-start" >Başarı Oranı</span ><span class="float-end">  {{basari_oarani}}-100%</span></label>
          <Slider  class="slider-blue"  v-model="basari_oarani" :step="10" :min="0" :max="100"  :tooltips="false"/>
       </div>
       
    
    


  <button type="reset" class="btn btn-outline-primary">Clear</button> 
  <button type="submit" class="btn btn-primary mx-2">Submit</button>
      
    
</div>
   
</template>


<script>
  import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap"
  import Slider from '@vueform/slider'

export default {
  components: {
    Slider,
  },
  data() {
    return {
      kumulatif_pnl: 0,
      hesap_varliklari:0,
      takipciler:[0,3000],
      kumulatif_kazanc:0,
      roi:0,
      risk:[0,9],
      basari_oarani:0,
      p_l_orani:1
    }
  }
}
  </script>
<style src="@vueform/slider/themes/default.css"></style>
<style scoped>
  .slider-blue {
  --slider-connect-bg: #3B82F6;
  --slider-tooltip-bg: #3B82F6;
  --slider-handle-ring-color: #3B82F630;
}
</style>