<p>
	This addon brings the power of NVIDIA OptiX Denoiser directly into Blender 3D. It has 4 simple features:
</p>

<ul>
	<li>Denoise render result</li>
	<li>Render and denoise result</li>
	<li>Denoise rendered animation</li>
	<li>Render animation and denoise</li>
</ul>

<p>
	It is built on top of a command line executable coded by Declan Russel (https://github.com/DeclanRussell/NvidiaAIDenoiser). 
	The addon automates the usage of this executable to use it directly from Blender.
</p>
<p>
	The two features of the addon that include rendering the image(s) before denoising disable any preview during the rendering process, and the UI will
	be frozen. This is why I recommend to render manually the image(s) and then click either  "Denoise render result" for a single image, or 
	"Denoise rendered animation".
</p>
<p>
	When you denoise a single image, either from option 1 or 2, the normal noisy rendered image is keeped into the "Render result", and a temporary file
	is created and opened to let you view the denoised result. It is then easy to compare the noisy and the denoised images! <b>This file is overwritten
	every time you denoise an image</b>, no matter in which project. That is to say, <b>if it is your final render, save it somewhere else</b>. <br/>
	When you denoise an animation, you must go in the folder where the frames are saved and view them here.
</p>
<p>
	When using the addon for an animation, it is required that you specify where the image will be saved on your disk, for the denoiser requires to know
	where the images will be stored in order to read them. The folder where you save the animation must be different of the default "/tmp\", to avoid
	any conflict with existing images. <br/>
	What's more, you must render your animation as an <b>image sequence</b>, not a video file, or the denoising won't work.
</p>
<p>
	This addon provides an access to the OptiX AI Denoiser, and thus has the same advantages, but also the same weaknesses. For instance, <b>it runs
	exclusively on NVIDIA GPUs</b>. Note that due to the use of an external executable, <b>it runs only on Windows</b>. Also, denoising a very low 
	sample image will result in strange results.
</p>
<br/>
<br/>
<p>
	<b><u>DOWNLOAD LINK:</u></b>https://drive.google.com/open?id=10WNZuG4oaMIyLn0Klay7_DpZw5GzYHGF
</p>
<p>
	Tested on Windows 8.1 64 bits, with Blender 2.79. 
</p>

<p>
	<b>Developpers</b>, if you want to modify this addon, I recommend you to download the release directly, for the script will be the same as on this 
	repository, and it will directly include the executable, which is not on the repository. The denoiser executable and all its dependencies must be
	in the "Denosier_v2.1" folder, which is placed in the same folder as the script, like this:
	<ul>
		<li>Denosier_v2.1/
			<ul>
				<li>...</li>
			</ul>
		</li>
		<li>icons/
			<ul>
				<li>optix_logo.png</li>
			</ul>
		</li>
		<li>
			blender_optix_denoiser.py
		</li>
	</ul>
</p>