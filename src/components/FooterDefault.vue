<script>
import SvgIcon from '@jamescoyle/vue-icon'
import { mdiGithub } from '@mdi/js'
import { mdiLinkedin } from '@mdi/js'
export default {
	name: "my-cool-component",

	components: {
		SvgIcon,
	},

	data() {
		return {
	  		path: mdiGithub,
	  		pathb: mdiLinkedin,
		}
	}
}
</script>

<template>
    <div class="footer" >
        <p class="text-footer">
            <svg-icon type="mdi" :path="path"></svg-icon> 
            <a class="text-footer" href="https://github.com/gabriel04alves">
                /gabriel04alves
            </a>
        </p>
        <p class="text-footer">
            <svg-icon type="mdi" :path="pathb"></svg-icon>
            <a class="text-footer" href="https://linkedin.com/in/gabriel04alves">
                /gabriel04alves
            </a>
        </p>
    </div>
</template>

<style>
.footer {
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    bottom: 0;
    width: 100%;
    gap: 1%;
    border-top: 0.25em solid;
    border-image: linear-gradient(60deg, #52b0cf, #8a2be2) 1 1;
    color: #F4F4F4; 
    background-color: #002F40;
    padding: 1%;
}

.text-footer {
    font-family:'Raleway', 'Times New Roman', Times, serif;;
    text-decoration: none;
    color: #f4f4f4;
    font-weight: 300;
    margin-top: 2px;
    display: flex;
    justify-content: center;
    gap: 2.5px;
    font-size: 1.7vh;
}
</style>