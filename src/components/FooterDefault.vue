<template>
    <footer class="footer" >
        <div class="footer-container">
            <a href="https://github.com/gabriel04alves" class="item-footer">
                <svg-icon type="mdi" :path="path"></svg-icon> 
                /gabriel04alves
            </a>
            <a href="https://linkedin.com/in/gabriel04alves" class="item-footer">
                <svg-icon type="mdi" :path="pathb"></svg-icon>
                /gabriel04alves
            </a>
        </div>
    </footer>
</template>

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

<style>
footer {
    display: flex;
    justify-content: center;
    width: 100%;
}

.footer-container {
    display: flex;
    justify-content: center;
    position: fixed;
    bottom: 0;
    
    border-radius: 20px;
    padding: 1rem 5rem;
    margin: 1rem;
    gap: 2vw;
    
    background-color: #002F40;
}

.item-footer {
    font-family:'Raleway', 'Times New Roman', Times, serif;;
    text-decoration: none;
    font-weight: 300;
    color: #f4f4f4;

    display: flex;
    align-items: center;
}
</style>