<template>
    <menu class="menu-mobile">
        <!--img id="menuIcon" v-bind:src=this.icon @click="toggleIcon()" alt="hamburger-icon"/>-->
		<img id="menuIcon" src='../assets/burger-menu.svg' @click="toggleIcon()" alt="hamburger-icon"/>
		<img id="menuIcon" src='../assets/burger-menu.svg' @click="toggleIcon()" alt="hamburger-icon"/>
        <ul :class="[this.activate ? 'activate' : 'deactivate']" id="menu-content">
            <p><u>Menú</u></p>
            <li><a href="./">Main</a></li>
            <li><a href="./about">About me</a></li>
            <li><a href="./portfolio">Portfolio</a></li>
            <li><a href="#">Posts</a></li>
            <li><a href="./contact">Contact</a></li>
        </ul>
    </menu>
	<menu class="menu-desktop">
		<ul id="menu-content">
            <li><a href="./">Main</a></li>
            <li><a href="./about">About me</a></li>
            <li><a href="./portfolio">Portfolio</a></li>
            <li><a href="#">Posts</a></li>
            <li><a href="./contact">Contact</a></li>
        </ul>
	</menu>
</template>
<script>

export default {
    name: "mobileMenu",
    data: function() {
        return {
                icon: '../assets/burger-menu.svg',
				activate: false
            };
    },
    methods: {
        toggleIcon() {

			if(this.icon == '../assets/burger-menu.svg') {
				this.icon = '../assets/burger-menu-orange.svg';
				this.activate = true
			} else {
				this.icon = '../assets/burger-menu.svg';
				this.activate = false
			}
        }
    }
}
</script>
<style>
@import '../styles/config.css';

.menu-desktop {
	display: none;
}

.menu-mobile {
	width: 100%;
	height: auto;
	position:fixed;
	top: 0;
	left: -40vw;
	transition: all .5s ease;
	z-index: 1;
}

.menu-mobile img {
	cursor: pointer;
	width: 15%;
	margin-left: 4.5rem;
	transform: scale(1.5);
	height: auto;
}

.menu-mobile ul {
	background-color: var(--just-black);
	padding: 6% 20% 2% 0%;
	list-style: none;
	position: absolute;
	top: 0;
	left: 0;
	transition: all .5s ease;
	z-index: -1;
}

.menu-mobile li a, .menu-mobile p {
	text-decoration: none;
	padding: 6% 20%;
	margin: 3rem 0;
	color: var(--just-white);
	display: block;
	font-size: xx-large;
	cursor: pointer;
}


.menu-mobile li a:hover {
	color: var(--fresh-red);
} 


.activate {
	transform: translate(56%);
}
.deactivate {
	transform: translate(-200px);
}

.opacity {
	background-color: var(--black);
	transition: .5s ease;
}

@media screen and (min-width: 760px) {

	.menu-mobile ul {
		padding: 6% 10% 2% 2%;
	}

	.menu-mobile li a, .menu-mobile p {
		padding: 6% 20%;
	}

	.activate {
		transform: translate(110%);
	}

}

@media screen and (min-width: 1024px) {

	.menu-mobile {
		display: none;
	}

	.menu-desktop {
		display: block;
		margin-top: 5rem;
		margin-bottom: 15rem;
	}

	.menu-desktop ul {
		list-style: none;
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		margin: 4rem 0rem;
	}

	.menu-desktop ul li a {
		text-decoration: none;
		color: var(--just-white);
		font-size: x-large;
		font-weight: bold;
	}

	.menu-desktop li a:hover {
		color: var(--fresh-red);
	} 

}
</style>