## Additional info by LL

Where to get some dependencies:

(See "Automatic Installation" on the main README.md on where to place each )

SD model checkpoints: 
	- place at models/Stable-diffusion
	- 1.x:
		- 1.4: https://huggingface.co/CompVis/stable-diffusion-v-1-4-original
	- 2.x:
		- Additional info: 
			- Some additional YAML files are necessary: https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies 
			- Download and place under the same name in the same folder
		- Versions:
			- 2.0: https://huggingface.co/stabilityai/stable-diffusion-2
			- 2.1: https://huggingface.co/stabilityai/stable-diffusion-2-1
			- (there might be a newer version, check stabilityai's page)
		- Is it better?:
			- Generally better, but it's more restricted in certain areas (anatomy, celebrities, nudity)
			- All existing prompts for version 1 will not work the same for version 2. The input prompt needs to be a little more descriptive
			- Since Stable Diffusion is trained on subsets of LAION-5B, there is a high chance that OpenCLIP will train a new text encoder using LAION-5B in the future. Given that the text encoder is a crucial component in the entire stable diffusion architecture, most of the existing works related to prompts will be invalidated when the text encoder changed
			- Source: https://towardsdatascience.com/stable-diffusion-2-the-good-the-bad-and-the-ugly-bd44bc7a1333
	
GFPGANv1.4.pth: 
	- place at root
	- https://upscale.wiki/wiki/Official_Research_Models

	
Troubleshooting:
	At leas on Windows: if using pyenv (https://github.com/pyenv/pyenv) or pyenv-win (https://github.com/pyenv-win/pyenv-win), you have to specify the python executable in webui-user.bat, AND you have to install a non-win32 python version
		For ex. in webui-user.bat, set PYTHON="C:\Users\lucianmq\.pyenv\pyenv-win\versions\3.10.6"