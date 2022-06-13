<template>
	<header class="header">
  		<div class="container">
  			<div class="header__wrapper">
  				<div class="header__main-content">
  					<a href="#" class="logo">
  						Logo
  					</a>
  					<ul class="header__navbar">
  						<li 
  							class="header__item"
  							v-for="item in headerItems"
  							:key="item.id"
  						>
  							<router-link 
  								:to="item.url" 
  								active-class="active"
  								class="header__link"
  							>
  								{{item.text}}
  							</router-link>
  						</li>
  					</ul>
  				</div>

  				<a href="#" class="header__contact">
  					<img src="@/assets/img/phone.png" alt="телефон">
  					+7 (988) 777-54-54
  				</a>
  			</div>
  		</div>
	</header>

	<header class="header-mob">
		<div class="container">
			<div class="header-mob__wrapper">
				<a href="#" class="logo">
  					Logo
  				</a>

  				<div class="nav-btn">
  					<div></div>
  					<div></div>
  					<div></div>
  				</div>
			</div>
		</div>
	</header>
</template>

<script>
	export default {
  		data() {
  			return {
  				headerItems: [
  					{id: 1, text: 'Главная', url: '/', active: true},
  					{id: 2, text: 'Направления', url: '/direction', active: false},
  					{id: 3, text: 'Педагоги', url: '/teachers'},
  					{id: 4, text: 'Цены и расписания', url: '/prices-and-schedules', active: false},
  					{id: 5, text: 'Контакты', url: '/contacts', active: false},
  				]
  			}
  		}
	}
</script>