<script>
    const urls = import.meta.glob("../../static/images/cases/*.jpg");
    console.log(urls);
</script>

<header>
    <div class="flex-container center-x-y menu">
        <!-- <nav>
            <button>Menu Button</button>
            <ul>
                <li>Menu Item 1</li>
                <li>Menu Item 2</li>
                <li>Menu Item 3</li>
            </ul>
        </nav> -->
        <div class="flex-container phone-select hidden">
            <select>
                <option value=0>Select Phone:</option>
                <option value="iPhone">iPhone</option>
                <option value="iPhone">Android</option>
            </select>
            <select>
                <option value="0">Model:</option>
                <option value="1">iPhone SE</option>
                <option value="2">iPhone 13 Pro / Max</option>
                <option value="3">iPhone 13</option>
                <option value="4">iPhone 13 Mini</option>
                <option value="5">iPhone 12 Pro Max</option>
                <option value="6">Samsung </option>
                <option value="7">Land Rover</option>
                <option value="8">Mercedes</option>
                <option value="9">Mini</option>
                <option value="10">Nissan</option>
                <option value="11">Toyota</option>
                <option value="12">Volvo</option>
            </select>
        </div>
    </div>
    <div class="flex-container center-x-y logo">Logo</div>
    <div class="flex-container center-x-y options">Cart
        <div id="smart-button-container">
      <div style="text-align: center;">
        <div id="paypal-button-container"></div>
      </div>
    </div>
  <script src="https://www.paypal.com/sdk/js?client-id=Aee5uX1s_iSc0haQ1JK4UF_xktrPyooYhOIz7yfgv1NXFhZdMXZUPMEAiq1K5mzxOFvqPInbGFLDU5Sx&enable-funding=venmo&currency=USD" data-sdk-integration-source="button-factory"></script>
  <script>
    function initPayPalButton() {
      paypal.Buttons({
        style: {
          shape: 'pill',
          color: 'blue',
          layout: 'vertical',
          label: 'checkout',
          
        },

        createOrder: function(data, actions) {
          return actions.order.create({
            purchase_units: [{"description":"Kate's Custom Phone Case","amount":{"currency_code":"USD","value":25}}]
          });
        },

        onApprove: function(data, actions) {
          return actions.order.capture().then(function(orderData) {
            
            // Full available details
            console.log('Capture result', orderData, JSON.stringify(orderData, null, 2));

            // Show a success message within this page, e.g.
            const element = document.getElementById('paypal-button-container');
            element.innerHTML = '';
            element.innerHTML = '<h3>Thank you for your payment!</h3>';

            // Or go to another URL:  actions.redirect('thank_you.html');
            
          });
        },

        onError: function(err) {
          console.log(err);
        }
      }).render('#paypal-button-container');
    }
    initPayPalButton();
  </script>

    </div>
</header>
<main>
    <div class="flex-container flex-wrap cases">
        <div class="flex-item flex-column flex-percent-25 flex-container center-x" itemscope>
            <figure>
                <img src="/images/cases/butterfly-blue.jpg" alt="" itemprop="Case Image">
                <figcaption>Butterfly <br><span>Blue</span></figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/checkerboard-black-white.jpg" alt="" itemprop="Case Image">
                <figcaption>Checkerboard <br><span>Black & White</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/checkerboard-green-white.jpg" alt="" itemprop="Case Image">
                <figcaption>Checkerboard <br><span>Green & White</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/checkerboard-wavy-hotpink-white.jpg" alt="" itemprop="Case Image">
                <figcaption>Wavy Checkerboard <br><span>Hot Pink & White</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/checkerboard-wavy-lightpink-white.jpg" alt="" itemprop="Case Image">
                <figcaption>Wavy Checkerboard <br><span>Light Pink & White</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/flowers-blue.jpg" alt="" itemprop="Case Image">
                <figcaption>Flowers <br><span>Blue</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/flowers-yellow.jpg" alt="" itemprop="Case Image">
                <figcaption>Fowers <br><span>Yellow</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/hat-pink.jpg" alt="" itemprop="Case Image">
                <figcaption>Hat <br><span>Pink</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/heart-darkblue.jpg" alt="" itemprop="Case Image">
                <figcaption>Heart <br><span>Dark Blue</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/heart-green.jpg" alt="" itemprop="Case Image">
                <figcaption>Heart <br><span>Green</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/smile-pink.jpg" alt="" itemprop="Case Image">
                <figcaption>Smiley <br><span>Pink</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
        <div class="flex-item flex-column flex-percent-25 flex-container center-x">
            <figure>
                <img src="/images/cases/waves-blue.jpg" alt="" itemprop="Case Image">
                <figcaption>Waves <br><span>Blue</span> </figcaption>
            </figure>
            <p class="price" itemprop="price"><span class="currency-type" content="USD">$</span><span class="price-amount" itemprop="amount">25</span></p>
        </div>
    </div>
</main>
<footer>
    <p>&copy 2022 katescases.com</p>
</footer>

<style lang="scss">
    .cases {
        .flex-item {
            padding: 3rem;
        }
        figure {
            flex: 0 0 auto;
            width: 100%;
            text-align: center;
            figcaption {
                font-size: 1.2rem;
                text-align: center;
                padding: 1rem 0 0.3rem;
                span {
                    display: inline-block;
                    padding: 0.5rem 0;
                    font-size: 1rem;
                }
            }
        }
        & img {
            max-width: 236px;
            width: 100%;
            border-radius: 20px;
        }
        .price {
            display: flex;
            flex: 0 0 auto;
            font-size: 3rem;
            font-weight: bold;
            transform: translateX(-0.6rem);
        }
        .currency-type {
            font-size: 1.6rem;
            display: inline-block;
            padding: 0.5rem 0.2rem;
        }
    }
</style>