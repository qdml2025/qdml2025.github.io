<script>
    import { Card, Carousel, Heading, P, Hr, Timeline, TimelineItem, Button, List, Li, Span, A } from 'flowbite-svelte';
    import { ArrowRightOutline, CalendarWeekSolid, ClockSolid } from 'flowbite-svelte-icons';
    import rhai from '$lib/assets/img/people/rhai.png';
    import kpark from '$lib/assets/img/people/kpark.jpg';
    import tlittau from '$lib/assets/img/people/tlittau.png';
    import home_bg from '$lib/assets/img/home_bg.jpg';

    export const sponsors = [
        {
            alt: 'SDT',
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
        <TimelineItem title="Paper Submission Deadline" date="February 25, 2025">
            <svelte:fragment slot="icon">
                <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-slate-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-slate-900">
                    <CalendarWeekSolid class="w-4 h-4 text-gray-900 dark:text-gray-200" />
                </span>
            </svelte:fragment>
            <Button href="https://easychair.org/my/conference?conf=qdml2025" color="alternative">Submit<ArrowRightOutline class="ms-2 w-5 h-5" /></Button>
        </TimelineItem>
        <TimelineItem title="Notification of Authors" date="March 14, 2025">
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
        <Li><Span bold>Abstracts:</Span> 1 page. Abstracts may summarize previously published work. Please explicitly cite your previous work.</Li>
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
    <div class="max-w-4xl items-center">
        <Carousel images={sponsors} duration="3000" />
    </div>  
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

<div id="program" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Program</Heading>
    <Hr classHr="my-8" />

    <Timeline order="vertical">
        <TimelineItem title="Expert Keynote Talks" date="">
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
        </TimelineItem>
    </Timeline>

</div>

<div id="papers" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Accepted Papers</Heading>
    <Hr classHr="my-8" />
    <Heading tag="h5" class="mb-4" customSize="text-xl font-extrabold  md:text-2xl lg:text-3xl">TBD</Heading>

</div>

<div id="committee" class="m-8 p-12 border-solid border-2 border-gray-950 rounded-lg bg-white dark:bg-gray-800">
    <Heading tag="h1" class="mb-4" customSize="text-center text-2xl font-extrabold  md:text-3xl lg:text-4xl">Committee</Heading>
    <Hr classHr="my-12" />

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
