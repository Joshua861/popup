<script>
	import Share from './share.svelte';
	import Footer from './footer.svelte';
	import Ad2 from './ad2.svelte';
	import Thanks from './thanks.svelte';
</script>

<br />
<article
	class="p-3 prose lg:prose-lg xl:prose-xl 2xl:prose-2xl dark:prose-invert mx-auto prose-img:rounded-xl"
>
	<h1>Lorem Ipsum</h1>
	<p>
		Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam in enim vel diam tristique varius
		a eu erat. Vestibulum et neque nunc. Vestibulum et ultricies sapien, vitae hendrerit mi.
		Phasellus sagittis lobortis imperdiet. Duis velit lacus, lacinia ut tincidunt sed, efficitur
		eget tortor. Integer et lacus at erat cursus accumsan. Vivamus eget velit elit. Sed nec mauris
		hendrerit, placerat odio eget, posuere nulla. Sed placerat tristique sem iaculis vehicula. Donec
		sit amet justo facilisis, porta velit eget, eleifend ante.
	</p>
	<figure>
		<img
			src="https://images.pexels.com/photos/574071/pexels-photo-574071.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
			alt="Someone coding on a laptop"
		/>
		<figcaption>
			Photo by <a href="https://www.pexels.com/photo/person-encoding-in-laptop-574071/">Lukas</a> from
			Pexels
		</figcaption>
	</figure>
	<p>
		Sed eget efficitur risus. Ut pellentesque ligula fermentum massa cursus, a vulputate mauris
		volutpat. In placerat diam non magna posuere, non dignissim quam lobortis. Donec elementum
		blandit orci, in viverra augue pulvinar vitae. Quisque ut nibh venenatis, euismod neque viverra,
		varius ante. Fusce nunc tortor, consectetur ut leo quis, dapibus scelerisque enim. Fusce tempor
		elit at dui rutrum, ut mattis metus porttitor.
	</p>
	<Ad2 />
	<p>
		Proin vitae lacinia diam, et rhoncus metus. Suspendisse vel mollis quam. Nam cursus sem nec
		aliquet sodales. Quisque sit amet massa ornare, porta quam vitae, fringilla risus. Phasellus
		tincidunt mollis libero vel venenatis. Integer porttitor interdum augue, eget placerat turpis
		vestibulum a. Duis accumsan ante nec lobortis mollis.
	</p>
	<ul>
		<li>
			<strong>Lorem ipsum dolor</strong>: sit amet consectetur adipisicing elit. Praesent fringilla
			vehicula augue, sit amet rutrum orci dignissim nec.
		</li>
		<li>
			<strong>Aliquam tortor mi</strong>: vehicula eget justo non, gravida aliquet leo. Vestibulum
			tristique libero tortor. Sed commodo at nisl in finibus. Donec vel maximus dui, sit amet
			dapibus sem.
		</li>
		<li>
			<strong>Sed vel justo vitae urna</strong>: molestie aliquet aliquam in nunc. Morbi sed luctus
			ligula. Nunc faucibus porttitor erat, eu lobortis ipsum mollis sed.
		</li>
	</ul>
	<p>
		Curabitur vel velit sed augue imperdiet vulputate vel ut urna. Orci varius natoque penatibus et
		magnis dis parturient montes, nascetur ridiculus mus. Curabitur id tincidunt sem. Sed nec
		vehicula felis, ut pulvinar quam. Fusce vel dictum libero. Aenean cursus nunc nec porttitor
		blandit. Sed interdum commodo tortor mattis finibus. Sed tempor elit nisi, in bibendum mi
		bibendum ac.
	</p>
	<figure>
		<img
			src="https://images.pexels.com/photos/1181263/pexels-photo-1181263.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
			alt="To people looking at code on a laptop"
		/>
		<figcaption>
			Photo by Christina <a
				href="https://www.pexels.com/photo/two-women-looking-at-the-code-at-laptop-1181263"
				>Morillo</a
			> from Pexels/
		</figcaption>
	</figure>
	<p>
		Suspendisse pharetra pellentesque finibus. Praesent sit amet gravida nulla. Etiam id euismod
		ligula. Nam convallis posuere risus, vitae bibendum metus accumsan eget. Donec a purus mauris.
		Maecenas sed felis eget ligula pellentesque bibendum.
	</p>
	<Share />
	<br />
	<Thanks />
	<Footer />
</article>
