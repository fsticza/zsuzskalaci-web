<template>
  <div class="section__title--wrapper">
    <h1 :class="['section__title', titleClass]">
      <span class="decor">
        <span class="decor__image">
          <svg version="1.1"  xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
            width="559.789px" height="559.789px" viewBox="0 0 559.789 559.789"
            xml:space="preserve">
            <g>
              <g>
                <path fill="currentColor" d="M337.586,146.282h-0.125c0,0-16.602-18.695-31.098-5.183c-14.496,13.512-1.807,44.542,31.098,58.054l0.125,0.019
                  c32.904-13.512,45.584-44.561,31.096-58.073C354.195,127.587,337.586,146.282,337.586,146.282z"/>
                <path  fill="currentColor" d="M479.799,268.672c-21.764-80.517-111.652-30.438-111.652-30.438l-44.408-10.098l23.629,45.202
                  c-9.16,51.876,21.803,86.665,21.803,86.665c15.951,19.929,37.619,31.355,60.627,37.504v26.087h9.562v-23.82
                  c6.35,1.291,12.746,2.189,19.125,2.821v20.999h9.562v-20.253c48.117,2.648,91.742-10.127,91.742-10.127
                  C514.797,386.358,498.006,347.591,479.799,268.672z M394.129,262.82c-6.092,0.039-11.055-4.877-11.094-10.968
                  c-0.037-6.091,4.877-11.054,10.969-11.092s11.055,4.877,11.092,10.968C405.125,257.819,400.219,262.782,394.129,262.82z"/>
                <path  fill="currentColor" d="M171.599,423.594h9.562v-26.307c23.132-8.032,44.408-20.568,60.731-39.646c0,0,38.862-40.832,26.479-100.923
                  l29.396-52.814l-56.324,12.364c0,0-115.008-56.849-141.535,36.931C77.887,345.067,57.098,390.307,0,398.914
                  c0,0,72.493,18.542,142.912,7.697v16.983h9.562v-18.656c6.445-1.253,12.833-2.783,19.125-4.609V423.594z M215.529,222.686
                  c7.201-0.038,13.072,5.757,13.11,12.957c0.038,7.201-5.757,13.072-12.958,13.11c-7.2,0.038-13.072-5.756-13.11-12.957
                  C202.534,228.596,208.338,222.734,215.529,222.686z"/>
              </g>
            </g>
          </svg>
        </span>
      </span>
      <slot></slot>
    </h1>
  </div>
</template>

<script>
export default {
  props: {
    titleClass: String
  }
}
</script>

<style lang="scss">
 @import '../assets/styles/abstracts/variables';

.section__title {
  margin-top: 4rem;
  display: inline-block;
  background-color: transparentize($primary, 0.9);
  color: #848383;
  padding: 1rem 2rem 0.5rem;
  margin-bottom: 4rem;
  font-family: $font-family-cursive;
  font-size: 2.5rem;
  line-height: 2.5rem;
  border-top: 2px solid transparentize($primary, 0.9);
  border-bottom: 2px solid transparentize($primary, 0.9);
}

.section__title--light {
  background-color: transparentize(#fff, 0.9);
  color: #fff;
  border-top: 2px solid transparentize(#fff, 0.9);
  border-bottom: 2px solid transparentize(#fff, 0.9);

  .decor {
    color: #fff;
  }
}
.section__title--wrapper {
  position: relative;
  text-align: center;
}
.decor {
  position: absolute;
  left: 50%;
  top: -10px;
  margin-left: -28px;
  color: $primary;
  opacity: 0.6;
  border-bottom: 1px dotted;

  &:after {
    content: '';
    position: absolute;
    bottom: -22px;
    width: 0;
    height: 20px;
    border-right: 1px dotted;
    left: 50%;
  }
}
.decor__image {
  display: inline-block;
  height: 50px;

  svg {
    transform: scale(1.1);
    height: 56px;
    width: 56px;
  }
}

</style>
