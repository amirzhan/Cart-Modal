<template>
  <div class="cart-modal">
		<div class="cart-modal_header">
			<div class="cart-modal__info">
				<div class="cart-modal__info-text">
					Товар успешно добавлен<span class="icon-success cart-modal__icon-success"></span>
				</div>
				<div class="cart-modal__total-price">
					В вашей корзине 1 товар 113 999 ₸
				</div>
				<div class="icon-close cart-modal__icon-close"></div>
			</div>
		</div>
		<div class="cart-modal_product-info">
			<div class="cart-modal__product-photo-and-name">
				<div class="cart-modal__product-photo"></div>
				<div class="cart-modal__product-name">{{product.name}}</div>
			</div>
			<div class="number-selector cart-modal__number-selector">
				<input type="text" class="number-display cart-modal__number-display" :value="count" @keyup="increment">
				<div class="up-down-buttons cart-modal__up-down-buttons">
					<div class="button-up" @click="product.count++"></div>
					<div class="button-down" @click="product.count--"></div>
				</div>
			</div>
			<div class="cart-modal__product-price"><span class="big-price">113</span><span class="medium-price">999</span><span class="medium-price">₸</span></div>
		</div>
		<div class="cart-modal_cart-actions"> 
			<a href="#" class="cart-modal__continue">Продолжить покупки</a>
			<button class="cart-modal__go-to-cart-button">Перейти в корзину</button>
		</div>
		<div class="cart-modal__shadow-box"></div>
  </div>
</template>

<script>
export default {
  data () {
    return {
    	product: {
    		name: 'Зеркальный фотоаппарат Nikon D3400 Kit',
    		count: 1,
    		price: 113999
    	}
    }
  },
  methods: {
  	increment: function() {
  		console.log('keyup')
  		this.product.count = document.getElementsByClassName('number-display')[0].value
  	}
  },
  computed: {
  	count: function() {
  		if (this.product.count<=0) this.product.count = 1;
  		return this.product.count;
  	}
  }
}
</script>

