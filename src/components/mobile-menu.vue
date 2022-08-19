<template>
    <menu class="menu-mobile">
        <img id="menuIcon" src="../assets/burger-menu.svg" @click="toggleIcon()" alt="hamburger-icon"/>
        <ul class="activate" id="menu-content">
            <p><u>Menú</u></p>
            <li><a href="#">Main</a></li>
            <li><a href="./html/about.html">About me</a></li>
            <li><a href="./html/portfolio.html">Portfolio</a></li>
            <li><a href="#">Posts</a></li>
            <li><a href="./html/contact.html">Contact</a></li>
        </ul>
    </menu>
</template>
<script>
export default {
    name: "mobileMenu",
    data: function() {
        return {
                icon: '/assets/burger-menu.svg',
            };
    },
    methods: {
        toggleIcon() {
           return this.icon = '/assets/burger-menu-orange.svg';
        }
    }
}
</script>
<style>
@import '../styles/config.css';

.menu-mobile {
	width: 100%;
	height: auto;
	position: fixed;
	top: 5vw;
	left: -40vw;
	transition: all .5s ease;
	z-index: 1;
}

.home .menu-mobile img {
	cursor: pointer;
	vertical-align: top;
	width: 15%;
	transform: scale(1.5);
	height: auto;
}

.menu-mobile ul {
	background-color: var(--just-black);
	padding: 10% 20% 2% 0%;
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
	transform: translate(-600px);
}

.opacity {
	background-color: var(--black);
	transition: .5s ease;
}
</style>