<template>
    <header class="header">
        <div class="title-container">
            <h1 class="title">  
                <svg-icon type="mdi" :path="path" style="zoom: 150%;"></svg-icon> 
                <p><RouterLink class="item-page-link" active-class="active" to="/">Fun Advice App</RouterLink></p> 
            </h1>
        </div>
        <div class="subtitle-container">
            <h2 class="subtitle">
                <svg-icon type="mdi" :path="pathb" style="zoom: 120%;"></svg-icon> 
                <RouterLink class="item-page-link" active-class="active" to="/about">About</RouterLink>
            </h2>
        </div>
    </header>
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
.header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: row;
        
        padding: 1.5rem;
        margin: 1rem;
        border-radius: 20px;
        
        background-color: #002F40;
        font-family: 'Raleway', 'Times New Roman', Times, serif;
    }

    .title, .subtitle {
        display: flex;
        align-items: center;

        font-weight: 400;
        font-size: 1rem;

        color: #F7F7F7;
    }

    .subtitle {
        gap: 5px;
    }
    
    .item-page-link {
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
