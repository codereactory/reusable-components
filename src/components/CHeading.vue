<script>
import { headingNumbering } from '../validators'
export default {
  name: 'c-heading',

  props: {
    level: {
      type: [Number, String],
      default: 1,
      headingNumbering,
    },
    as: {
      type: [Number, String],
      headingNumbering,
    },
    large: {
      type: Boolean,
      default: false,
    },
  },

  render(createElement) {
    return createElement(
      'h' + this.level,
      {
        class: {
          [this.large ? `display-${this.as}` : `h${this.as}`]: !!this.as,
        },
      },
      this.$slots.default)
  },
}
</script>

<style>
h1, h2, h3, h4, h5, h6,
.h1, .h2, .h3, .h4, .h5, .h6 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-weight: 500;
  line-height: 1.2;
}

h1, .h1 { font-size: 2.5rem; }

h2, .h2 { font-size: 2rem; }

h3, .h3 { font-size: 1.75rem; }

h4, .h4 { font-size: 1.5rem; }

h5, .h5 { font-size: 1.25rem; }

h6, .h6 { font-size: 1rem; }

.display-1 {
  font-size: 6rem;
  font-weight: 300;
  line-height: 1.2; 
}

.display-2 {
  font-size: 5.5rem;
  font-weight: 300;
  line-height: 1.2; 
}

.display-3 {
  font-size: 4.5rem;
  font-weight: 300;
  line-height: 1.2; 
}

.display-4 {
  font-size: 3.5rem;
  font-weight: 300;
  line-height: 1.2; 
}

.display-5 {
  font-size: 3.0rem;
  font-weight: 300;
  line-height: 1.2; 
}

.display-6 {
  font-size: 2.5rem;
  font-weight: 300;
  line-height: 1.2;
}
</style>