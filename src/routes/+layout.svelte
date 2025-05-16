<script>
    import "../app.css";
    import { page } from '$app/stores';
    import { 
        Navbar, NavBrand, NavLi, NavUl, NavHamburger,
        Footer, FooterCopyright, Modal, Button, Indicator, Avatar,
        DarkMode 
    } from 'flowbite-svelte';
    import qdml_logo from '$lib/assets/img/qdml_logo.png';
    import rhai from '$lib/assets/img/people/rhai.png';
    import kpark from '$lib/assets/img/people/kpark.jpg';
    import tlittau from '$lib/assets/img/people/tlittau.png';

    $: activeUrl = $page.url.pathname;

    /**
     * @param {{ preventDefault: () => void; currentTarget: any; }} event
     */
    function handleAnchorClick (event) {
		event.preventDefault()
		const link = event.currentTarget
		const anchorId = new URL(link.href).hash.replace('#', '')
		const anchor = document.getElementById(anchorId)
		window.scrollTo({
			// @ts-ignore
			top: anchor.offsetTop - 128,
			behavior: 'smooth'
		})
	}

    let contactModal = false;
</script>
<!-- <Navbar class="fixed bg-gray-900 rounded-lg mt-8 mb-8 w-full border-b-2 lg:m-8 dark:bg-gray-800"> -->
<Navbar class="px-2 bg-gray-900 text-white sm:px-4 py-2.5 fixed w-full z-20 top-0 start-0 border-b dark:bg-gray-800">
    <!-- <NavBrand href="/" class="hidden md:inline-flex">
        <img src="/qdml_logo.png" class="me-3 h-9" alt="QDML Logo" />
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Quantum Data and Machine Learning</span>
    </NavBrand> -->
    <NavBrand href="/">
        <img src={qdml_logo} class="me-3 h-9" alt="QDML Logo" />
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">QDML 2025</span>
    </NavBrand>
    <NavHamburger />
    <NavUl {activeUrl}>
        <NavLi class="md:text-white" href="#aims" on:click={handleAnchorClick}>Aims & Scope</NavLi>
        <NavLi class="md:text-white" href="#submit" on:click={handleAnchorClick}>Submission</NavLi>
        <NavLi class="md:text-white" href="#sponsors" on:click={handleAnchorClick}>Sponsors</NavLi>
        <NavLi class="md:text-white" href="#program" on:click={handleAnchorClick}>Program</NavLi>
        <NavLi class="md:text-white" href="#papers" on:click={handleAnchorClick}>Accepted Papers</NavLi>
        <NavLi class="md:text-white" href="#commitee" on:click={handleAnchorClick}>Organisation</NavLi>
        <NavLi class="md:text-white" href="/" on:click={() => (contactModal = true)}>Contact</NavLi>
    </NavUl>
    <DarkMode class="absolute right-12 top-2 lg:top-4" />
</Navbar>



<main>
    <div class="mt-32"></div>
    <slot />
</main>

<Modal title="Contact" bind:open={contactModal} autoclose>
    <p class="text-base leading-relaxed text-gray-500 dark:text-gray-400">Please contact us for any further information:</p>
    <ul class="max-w-sm divide-y divide-gray-200 dark:divide-gray-700 w-full">
        <li class="py-3 sm:py-4">
          <div class="flex items-center space-x-3 rtl:space-x-reverse">
            <Avatar src={rhai} href="mailto:r.hai@tudelft.nl" alt="Rihan image" />
            <div class="flex-1 min-w-0">
              <p class="text-sm font-semibold text-gray-900 truncate dark:text-white"><a href="mailto:r.hai@tudelft.nl">Rihan Hai</a></p>
              <p class="text-sm text-gray-500 truncate dark:text-gray-400"><a href="mailto:r.hai@tudelft.nl">r.hai@tudelft.nl</a></p>
            </div>
          </div>
        </li>
        <li class="py-3 sm:py-4">
          <div class="flex items-center space-x-3 rtl:space-x-reverse">
            <div class="flex-shrink-0">
              <Avatar src={kpark} href="mailto:kwanghyun.park@yonsei.ac.kr" alt="Kwanghyun image" />
            </div>
            <div class="flex-1 min-w-0">
              <p class="text-sm font-semibold text-gray-900 truncate dark:text-white"><a href="mailto:kwanghyun.park@yonsei.ac.kr">Kwanghyun Park</a></p>
              <p class="text-sm text-gray-500 truncate dark:text-gray-400"><a href="mailto:kwanghyun.park@yonsei.ac.kr">kwanghyun.park@yonsei.ac.kr</a></p>
            </div>
          </div>
        </li>
        <li class="py-3 sm:py-4">
            <div class="flex items-center space-x-3 rtl:space-x-reverse">
              <div class="flex-shrink-0">
                <Avatar src={tlittau} href="mailto:t.m.littau@tudelft.nl" alt="Tim image" />
              </div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-semibold text-gray-900 truncate dark:text-white"><a href="mailto:t.m.littau@tudelft.nl">Tim Littau</a></p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400"><a href="mailto:t.m.littau@tudelft.nl">t.m.littau@tudelft.nl</a></p>
              </div>
            </div>
          </li>
      </ul>
</Modal>
<Footer footerType="logo" class="bg-gray-900 lg:m-8 dark:bg-gray-800">
    <div id="contact" class="sm:flex sm:items-center sm:justify-between">
        
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
    <FooterCopyright href="https://www.wis.ewi.tudelft.nl" by="Web Information Systems, Delft University of Technology, Delft, The Netherlands" />
</Footer>


<style>
</style>