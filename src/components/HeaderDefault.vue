<template>
    <div class="all">
        <h1 class="title">  
            <svg-icon type="mdi" :path="path" style="zoom: 150%;"></svg-icon> 
            <p><RouterLink class="router-link" active-class="active" to="/">App-Conselhos</RouterLink></p> 
        </h1>
        <h2 class="subtitle">
            <svg-icon type="mdi" :path="pathb" style="zoom: 120%;"></svg-icon> 
            <RouterLink class="router-link" active-class="active" to="/about">About</RouterLink>
        </h2>
    </div>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon'
import { mdiLightbulbMultipleOutline } from '@mdi/js'
import { mdiInformationOutline } from '@mdi/js'
import { RouterLink } from 'vue-router'


export default {
	components: {
		SvgIcon,
        RouterLink
	},

	data() {
		return {
	  		path: mdiLightbulbMultipleOutline,
	  		pathb: mdiInformationOutline,
		}
	}
}
</script>

<style>

.all {
    background-color: #002F40;
    
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
    font-family: 'Raleway', 'Times New Roman', Times, serif;
    padding: 20px;
    border-bottom: 0.25em solid;
    border-image: linear-gradient(60deg, #8a2be2, #52b0cf) 1 1;
}

.title, .subtitle {
    display: flex;
    align-items: center;
    font-weight: 400;
    font-size: 3vh;
    color: #F7F7F7;
    display: flex;
    text-align: center;
    vertical-align: middle;
    flex-direction: row;
}
.subtitle {
    gap: 5px;
}
.router-link {
    color: #f7f7f7d0;
    font-weight: 300;
    font-size: 2vh;
    text-decoration: none;
}

.active {
    font-weight: 600;
    text-shadow: 1px #000;
}

</style>
