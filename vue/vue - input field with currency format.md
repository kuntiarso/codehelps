# Input Field with Currency Format

In this case, I want to add input field that directly change its format as currency number.

- Vue template:

  ```vue
  <v-text-field
      v-model="inputAmountFormat"
      label="Amount"
      prefix="Rp"
      @blur="inputAmountOut"
      @focus="inputAmountIn"
  />
  ```

- JS script:

  ```vue
  <script>
      export default {
          data: () => ({
              inputAmount: null,
              inputAmountFormat: null
          });
          methods: {
              inputAmountOut: function() {
                  this.inputAmount = parseFloat(this.inputAmountFormat.replace(/[^\d.]/g, ""));
                  if (isNaN(this.inputAmount)) {
                      this.inputAmount = null
                  }
                  this.inputAmountFormat = this.formatCurrency(this.inputAmount);
              },

              inputAmountIn: function() {
                  this.inputAmountFormat = this.inputAmount.toString();
              }
          }
      }
  </script>
  ```

That's all, hope this helps!

------

:wave: Hi, I'm @kuntiarso :green_book: Frontend Vuejs
