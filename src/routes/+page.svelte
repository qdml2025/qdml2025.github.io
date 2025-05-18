<script>
    import { Card, Carousel, Heading, P, Hr, Timeline, TimelineItem, Button, List, Li, Span, A } from 'flowbite-svelte';
    import { ArrowRightOutline, CalendarWeekSolid, ClockSolid, HourglassSolid } from 'flowbite-svelte-icons';
    import rhai from '$lib/assets/img/people/rhai.png';
    import kpark from '$lib/assets/img/people/kpark.jpg';
    import tlittau from '$lib/assets/img/people/tlittau.png';
    import tcoopmans from '$lib/assets/img/people/tcoopmans.jpeg';
    import fgeerts from '$lib/assets/img/people/fgeerts.jpg';
    import shung from '$lib/assets/img/people/shung.jpg';
    import jlu from '$lib/assets/img/people/jlu.jpg';
    import vuotila from '$lib/assets/img/people/vuotila.jpg';
    import mschoenberger from '$lib/assets/img/people/mschoenberger.png';
    import jkim from '$lib/assets/img/people/jkim.png';
    import wmauerer from '$lib/assets/img/people/wmauerer.png';
    import sgroppe from '$lib/assets/img/people/sgroppe.jpg';
    import cpark from '$lib/assets/img/people/cpark.png';
    import isabek from '$lib/assets/img/people/isabek.jpg';
    import home_bg from '$lib/assets/img/home_bg.jpg';

    export const sponsors = [
        {
            alt: 'https://sdt.inc/en/',
            src: '/img/sponsors/SDTLogo.svg',
            title: 'SDTLogo'
        }
    ]

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
			top: anchor.offsetTop - 32,
			behavior: 'smooth'
		})
	}
</script>

<div id="home" class="bg-contain text-center m-8 p-12 border-solid border-2 border-gray-950 rounded-lg" style="background-image: url('{ home_bg }')">
    <Heading tag="h3" class="mb-4 text-white">First International Workshop on</Heading>
    <Heading tag="h1" class="mb-4 text-white" customSize="text-4xl font-extrabold  md:text-5xl lg:text-6xl">Quantum Data and Machine Learning:</Heading>
    <Heading tag="h2" class="mb-4 text-white">Systems, Theory and Hardware</Heading>
    <P class="text-xl text-center text-white">In conjunction with <a class="text-sky-300" href="https://ieee-icde.org/2025/">ICDE 2025</a></P>
</div>

<div id="aims" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Aims & Scope</Heading>
    <Hr classHr="my-16" />

    <P class="text-center">
        With the rapid advancements in quantum computing, a transformative synergy between the data management and quantum computing communities has emerged. 
    </P>
    <P class="text-center">
        Quantum computing offers unprecedented potential and a new perspective on classical problems in database domains, including query optimization, data integration, index selection, and transaction management. 
    </P>
    <P class="text-center">
        As we transition into the era of near-term quantum computing, new data management challenges arise, requiring innovative approaches and collaboration. 
    </P>
    <P class="text-center">
        This workshop aims to establish a comprehensive theoretical foundation while exploring practical methodologies and use cases to advance research and applications in these intersecting fields.    
    </P>
    <Hr classHr="my-16" />
    <Heading tag="h5" class="mb-4">Quantum Data Management</Heading>
    <Hr classHr="my-8" />
    <List tag="ul" class="space-y-4 text-gray-900 dark:text-gray-200 mb-8">
        <Li>Database acceleration using quantum computing techniques</Li>
        <Li>Data management systems (DBMSs, data lakes, lakehouses) for quantum computers and quantum internet</Li>
        <Li>Hybrid quantum-classical data processing</Li>
        <Li>Data processing for developing quantum hardware</Li>
        <Li>Data management systems for classical simulation and quantum simulation</Li>
        <Li>Scientific data management for quantum experiments</Li>
    </List>

    <Heading tag="h5" class="mb-2">Quantum Machine Learning</Heading>
    <Hr classHr="my-8" />
    <List tag="ul" class="space-y-4 text-gray-900 dark:text-gray-200 mb-12">
        <Li>Quantum algorithms for machine learning tasks</Li>
        <Li>Data encoding for quantum machine learning algorithms</Li>
        <Li>Quantum learning theory</Li>
        <Li>Quantum-inspired machine learning</Li>
        <Li>Fuzzy logic for quantum machine learning</Li>
    </List>

    <Heading tag="h5" class="mb-2">Data Engineering for Quantum Computing</Heading>
    <Hr classHr="my-8" />
    <P class="mb-12">Data engineering methods and techniques to improve quantum computing, e.g. quantum error correction</P>

    <Heading tag="h5" class="mb-2">Domain specific Applications</Heading>
    <Hr classHr="my-8" />
    <P class="mb-12">Application of quantum data management and quantum machine learning in domains like quantum sensing, quantum simulation and quantum chemistry, etc.</P>
</div>

<div id="submit" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Submission Timeline</Heading>
    <Hr classHr="my-8" />

    <Timeline order="vertical">
        <TimelineItem title="Paper Submission Deadline">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <CalendarWeekSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <Span class="line-through block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">February 4, 2025</Span>
            <Span class="line-through block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">February 25, 2025</Span>
            <Span class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">March 3, 2025</Span>
            <Button href="https://easychair.org/my/conference?conf=qdml2025" color="alternative">Submit<ArrowRightOutline class="ms-2 w-5 h-5" /></Button>
        </TimelineItem>
        <TimelineItem title="Notification of Authors" date="March 19, 2025">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <CalendarWeekSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
        </TimelineItem>
        <TimelineItem title="Camera-ready Version of accepted Papers" date="March 25, 2025">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <CalendarWeekSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
        </TimelineItem>
        <TimelineItem title="Date of the Workshop" date="May 19, 2025">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <CalendarWeekSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
        </TimelineItem>
    </Timeline>
    <Hr classHr="my-16" />

    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Submission Guidelines</Heading>
    <Hr classHr="my-8" />
    <P class='mt-8'>
        The workshop will accept both regular papers and short papers (work in progress, vision/outrageous ideas).
        The page limit for regular papers is 6 pages, and for short papers is 4 pages with unlimited references. 
        The papers will be uploaded as PDF files to the review system. Each paper will be reviewed by at least three reviewers from the program committee (PC).
        We will apply the same principles for handling conflicts of interest with PC members or workshop chairs at the ICDE conference.
    </P>
    <Hr classHr="my-8" />
    <P>
        We welcome submissions in the following categories:
    </P>
    <List tag="ul" class="space-y-4 text-gray-900 mb-8 mt-8 dark:text-gray-200">
        <Li><Span bold>Regular Papers:</Span> up to 6 pages</Li>
        <Li><Span bold>Short Papers</Span> (e.g. work in progress, vision papers, or outrageous ideas): up to 4 pages</Li>
        <Li><Span bold>Abstracts:</Span> 1 page. Abstracts may summarize previously published or early work. Please explicitly cite your previous work.</Li>
    </List>
    <P>
        For all submission types, references are unlimited, but appendices are not allowed.
    </P>
    <Hr classHr="my-8" />
    <Heading tag="h5" class="mb-2">Submission Process</Heading>
    <List tag="ul" class="space-y-4 text-gray-900 mb-8 mt-8 dark:text-gray-200">
        <Li>All papers must be submitted as <Span bold>PDF files</Span> via <A class="font-medium hover:underline" href='https://easychair.org/my/conference?conf=qdml2025'>EasyChair</A></Li>
        <Li>Papers should adhere to the <Span bold>IEEE formatting guidelines</Span> <A class="font-medium hover:underline" href="https://www.ieee.org/conferences/publishing/templates.html">(template available)</A></Li>
    </List>
    <Hr classHr="my-8" />
    <Heading tag="h5" class="mb-2">Review Process</Heading>
    <List tag="ul" class="space-y-4 text-gray-900 mb-8 mt-8 dark:text-gray-200">
        <Li>Submissions will be reviewed in a <Span bold>single-blind</Span> manner (reviewers know the identity of authors, but not vice versa).</Li>
        <Li>We will follow the same conflict-of-interest policies as the ICDE conference to ensure fair evaluation.</Li>
    </List>
</div>

<div id="sponsors" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Sponsors</Heading>
    <Hr classHr="my-12" />
    <div class="w-1/2 p-8 mx-[25%] rounded-lg dark:bg-white">
        <Carousel images={sponsors} duration="3000" let:Indicators let:Controls> 
            <a slot="slide" href="{sponsors[index]?.alt}" target="_blank" let:Slide let:index>
                <Slide image={sponsors[index]} />
            </a>
            <Indicators class="-my-16 border border-white rounded-md p-2 bg-black bg-opacity-50" />
            <!-- <Controls /> -->
        </Carousel>
    </div>   
</div>

<div id="program" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Program</Heading>
    <Hr classHr="my-8" />

    <Timeline order="vertical">
        <TimelineItem title="Welcome Messages" date="9:00 - 9:05">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Speaker: Kwanghyun Park</P>
        </TimelineItem>
        <TimelineItem title="Keynote: Explore the Impact of Quantum Computing Chip on Data Science and AI" date="9:05 - 10:05">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Speaker: Prof. Liu Ai-Qun</P>
        </TimelineItem>
        <TimelineItem title="Paper Presentation: Neural Quantum Embeddings with Multiple Control Variables" date="10:05 - 10:20">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Authors: Seungyeop Baik and Yo-Sub Han</P>
        </TimelineItem>
        <TimelineItem title="Paper Presentation: Optimizing Join Orders via Constrained Quadratic Models" date="10:20 - 10:30">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>(online)</P>
            <P>Authors: Hanwen Liu, Pranshi Saxena, Federico Spedalieri and Ibrahim Sabek</P>
        </TimelineItem>
        <Hr classHr="my-4" />
        <TimelineItem title="Coffee Break" date="10:30 - 11:00">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <HourglassSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P></P>
        </TimelineItem>
        <Hr classHr="my-4" />
        <TimelineItem title="Industry Talk" date="11:00 - 11:20">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P></P>
        </TimelineItem>
        <TimelineItem title="Keynote: Quantum Computational Advantage: Verification and Classical Simulation" date="11:20 - 12:00">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Speaker: Shih-Han Hung</P>
        </TimelineItem>
        <TimelineItem title="Paper Presentation: Data-centric Approach of Macroscopic Physical System with NISQ Quantum Computers" date="12:00 - 12:15">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Authors: Junyong Lee, Jeihee Cho, Hyeonseong Jung, Euimin Lee, Sangmin Lee, Shiho Kim and Yunah Choi</P>
        </TimelineItem>
        <TimelineItem title="Invited Talk: The Effect of Gate Selection in Overparameterized Quantum Circuits" date="12:15 - 12:30">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Jeihee Cho, Junyong Lee, Daniel Justice and Shiho Kim</P>
        </TimelineItem>
        <TimelineItem title="Invited Talk: Native Gate-Aware QAOA Ansatz" date="12:30 - 12:45">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Hyungseok Kim, Enhyeok Jang, Youngmin Kim and Won Woo Ro</P>
        </TimelineItem>



        <!-- <TimelineItem title="Expert Keynote Talks" date="">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Keynote by invited experts from industry and/or academia (45 minutes each)</P>
        </TimelineItem>
        <TimelineItem title="Technical Presentation Session 1" date="">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>First session of three technical presentations (15 - 25 minutes each)</P>
        </TimelineItem>
        <TimelineItem title="Technical Presentation Session 2" date="">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Second session of three technical presentations (15 - 25 minutes each)</P>
        </TimelineItem>
        <TimelineItem title="Technical Presentation Session 3" date="">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>Third session of three technical presentations (15 - 25 minutes each)</P>
        </TimelineItem>
        <TimelineItem title="Panel Discussion" date="">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <P>(one hour for the panel discussion)</P>
        </TimelineItem>
        <TimelineItem title="Socialising and Workshop Dinner" date="">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <ClockSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
        </TimelineItem> -->
    </Timeline> 

</div>

<div id="papers" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Accepted Papers</Heading>
    <Hr classHr="my-8" />
    <List tag="ul" class="space-y-4 text-gray-900 mb-8 mt-8 dark:text-gray-200">
        <Li><Span bold>Optimizing Join Orders via Constrained Quadratic Models (Abstract)</Span> Hanwen Liu, Pranshi Saxena, Federico Spedalieri and Ibrahim Sabek</Li>
        <Li><Span bold>The Effect of Gate Selection in Overparameterized Quantum Circuits</Span> Jeihee Cho, Junyong Lee, Daniel Justice and Shiho Kim</Li>
        <Li><Span bold>Native Gate-Aware QAOA Ansatz</Span> Hyungseok Kim, Enhyeok Jang, Youngmin Kim and Won Woo Ro</Li>
        <Li><Span bold>Neural Quantum Embeddings with Multiple Control Variables</Span> Seungyeop Baik and Yo-Sub Han</Li>
        <Li><Span bold>Data-centric Approach of Macroscopic Physical System with NISQ Quantum Computers</Span> Junyong Lee, Jeihee Cho, Hyeonseong Jung, Euimin Lee, Sangmin Lee, Shiho Kim and Yunah Choi</Li>
    </List>

</div>

<div id="commitee" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Commitee</Heading>
    <Hr classHr="my-8" />
    <Heading tag="h5" class="mb-4">Organising Committee</Heading>
    <Hr classHr="my-8" />
    <div class="grid grid-cols-2 mb-16">
        <Card img={rhai}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Rihan Hai</h3>
            <h5 class="mb-2 text-lg font-bold tracking-tight text-gray-900 dark:text-white">Organiser</h5>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Assistant Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Technology Delft, Netherlands</p>
            <Button href="https://rihanhai.com">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={kpark}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Kwanghyun Park</h3>
            <h5 class="mb-2 text-lg font-bold tracking-tight text-gray-900 dark:text-white">Organiser</h5>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Assistant Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ Yonsei University, South Korea</p>
            <Button href="https://cs.yonsei.ac.kr:59290/bbs/board.php?bo_table=eng2_1_a&wr_id=37">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>
    </div>

    <Heading tag="h5" class="mb-4">Programme Commitee</Heading>
    <Hr classHr="my-8" />
    <div class="grid grid-rows-4 grid-cols-3 place-content-center divide-y">
        <Card img={tcoopmans}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Tim Coopmans</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Assistant Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Technology Delft, Netherlands</p>
            <Button href="https://timcoopmans.com">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={fgeerts}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Floris Geerts</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Antwerp, Belgium</p>
            <Button href="https://fgeerts.github.io">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={sgroppe}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Sven Groppe</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Luebeck, Germany</p>
            <Button href="https://www.ifis.uni-luebeck.de/~groppe/">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={shung}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Shih-Han Hung</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Assisstant Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ National Taiwan University, Taiwan</p>
            <Button href="https://hungshihhan.github.io">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={jkim}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Joongheon Kim</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight"> Associate Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ Korea University, South Korea</p>
            <Button href="https://sites.google.com/view/aimlab-kuee/members/joongheonkim">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={jlu}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Jiaheng Lu</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Helsinki, Finland</p>
            <Button href="https://www.cs.helsinki.fi/u/jilu/">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={wmauerer}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Wolfgang Mauerer</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ OTH Regensburg, Germany</p>
            <Button href="https://www.lfdr.de/People/mauerer/">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={cpark}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Chae-Yeun Park</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Assistant Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ Yonsei University, South Korea</p>
            <Button href="https://chaeyeunpark.me">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={isabek}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Ibrahim Sabek</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Assistant Professor</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Southern California, USA</p>
            <Button href="https://viterbi.usc.edu/directory/faculty/Sabek/Ibrahim">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={mschoenberger}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Manuel Schoenberger</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Doctoral Student</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ OTH Regensburg, Germany</p>
            <Button href="https://www.lfdr.de/People/schoenberger/">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>

        <Card img={vuotila}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Valter Uotila</h3>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">PhD Student</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Helsinki, Finland</p>
            <Button href="https://valteruo.github.io">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>
    </div>

    <Heading tag="h5" class="mb-4">Workshop Chairs</Heading>
    <Hr classHr="my-8" />
    <div class="grid grid-rows-1 grid-cols-2 place-content-center divide-y">
        <Card img={tlittau}>
            <h3 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Tim Littau</h3>
            <h5 class="mb-2 text-lg font-bold tracking-tight text-gray-900 dark:text-white">Publicity Chair</h5>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">PhD student</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">@ University of Technology Delft, Netherlands</p>
            <Button href="https://tmlittau.github.io/tmlittau-portfolio">
            Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
            </Button>
        </Card>
    </div>
</div>
