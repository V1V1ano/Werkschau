<script>
    import NavHome from "$lib/components/nav/NavHome.svelte";
    import Button from "$lib/components/Buttons/Button.svelte";
    import KeyArea from "$lib/components/KeyArea.svelte";
    import PreviewFinished from "$lib/components/preview/PreviewFinished.svelte";
    import CardResponsibilities from "$lib/components/cards/CardResponsibilities.svelte";
</script>

<NavHome />

<div class="content">
    <!-- Top section text -->
    <div class="intro-grid">
        <div class="chapter">
            <h1>Hi there!</h1>
            <div class="chapter-intro">&#123; Who am I &#125;</div>
            <div class="highlight-text">
                I am an interface designer specializing in the visualization of
                data and information. I value research-driven projects that
                create meaningful results and grow out of user-centred processes
                fueled by curiosity, and fun teamwork. Here’s a peek into how I
                work and who I am as a designer.
            </div>
            <div class="more-about-wrap">
                <Button href="/about" type="internal"
                    >More about me :&#41;</Button
                >
            </div>
        </div>

        <!-- Button section text -->
        <div class="contact">
            <div class="chapter">
                <div class="chapter-intro">&#123; How to contact me &#125;</div>
                <div class="in-chapter">
                    <Button
                        href="mailto:vivien.serve@gmail.com"
                        type="external"
                    >
                        mail me: vivien.serve@gmail.com
                    </Button>
                    <Button
                        href="https://www.linkedin.com/in/vivien-serve-25aa4a17a/?originalSubdomain=de"
                        type="external"
                    >
                        or write a dm: LinkedIn
                    </Button>
                </div>
            </div>
        </div>
    </div>

    <!-- Glipmse at work section -->
    <div class="chapter">
        <div class="chapter-intro">&#123; A glimpse at my work &#125;</div>
        <!-- Project grid is used to align content in a grid on desktop -->
        <div class="project-grid">
            <div class="in-chapter">
                <KeyArea variant="narratives" />
                <PreviewFinished
                    href="/projects/zeit"
                    title="Data visualization for the news"
                    context="Internship DIE ZEIT"
                    year="2025"
                    mediaType="video"
                    videoSrcWebm="/project-images/ZEIT/proteine.webm"
                />
            </div>
            <div class="in-chapter">
                <KeyArea variant="conceptual" />
                <PreviewFinished
                    href="/projects/proLanes"
                    title="ProLanes • Order to Cash"
                    context="Studies"
                    year="2023/24"
                    mediaType="image"
                    mediaSrc="/project-images/ProLanes/Teaser.png"
                />
            </div>
        </div>
    </div>

    <!-- Key Areas -->
    <div class="chapter-key-areas">
        <div class="chapter-intro">&#123; Key Areas &#125;</div>
        <div class="in-chapter-cards">
            <CardResponsibilities
                text="&#123;A&#125; I design (and sometimes code)"
                keyArea="conceptual"
            />
            <CardResponsibilities
                text="&#123;B&#125; to create intruiging"
                keyArea="ui"
            />
            <CardResponsibilities
                text="&#123;C&#125; with a focus on"
                keyArea="narratives"
            />
            <CardResponsibilities
                text="&#123;D&#125; and interest in"
                keyArea="speculative"
            />
        </div>
    </div>

    <!-- More Work -->
    <div class="chapter">
        <div class="chapter-intro">&#123; More work &#125;</div>
        <div class="project-grid">
            <div class="in-chapter">
                <KeyArea variant="conceptual" />
                <PreviewFinished
                    href="/projects/coopComm"
                    title="Co-op.Comm "
                    context="Studies"
                    year="2023"
                    mediaType="image"
                    mediaSrc="/project-images/CoopComm/teaser.gif"
                />
            </div>
            <div class="in-chapter">
                <KeyArea variant="speculative" />
                <PreviewFinished
                    href="/projects/phygital"
                    title="From Phygital Layers to Fragmented Realities"
                    context="Studies"
                    year="2023/24"
                    mediaType="image"
                    mediaSrc="/project-images/Phygital/teaser.png"
                />
            </div>
            <div class="in-chapter">
                <KeyArea variant="narratives" />
                <PreviewFinished
                    href="/projects/readingRoom"
                    title="The City as a Reading Room"
                    context="Studies"
                    year="2024"
                    mediaType="image"
                    mediaSrc="/project-images/ReadingRooms/big_picture.png"
                />
            </div>
        </div>
    </div>
</div>

<style>
    .content {
        display: flex;
        flex-direction: column;
        gap: 48px;
        margin-bottom: 48px;
    }

    /* This needs to mimic content */
    .intro-grid {
        display: flex;
        flex-direction: column;
        gap: 48px;
    }

    .chapter {
        display: flex;
        flex-direction: column; /* vertical stacking */
        gap: 18px;
    }

    .chapter-key-areas {
        display: flex;
        flex-direction: column; /* vertical stacking */
        gap: 18px;
    }

    /* this needs to mimic chapter */
    .project-grid {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    .in-chapter {
        display: flex;
        flex-direction: column;
        gap: 8px;
    }

    /* For the responsibility cards, needs to mimic in-chapter */
    .in-chapter-cards {
        display: flex;
        flex-direction: column;
        gap: 8px;
    }

    @media (min-width: 900px) {
        .project-grid {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            align-items: start;
            gap: 36px;
        }

        .chapter {
            gap: 24px;
        }

        .in-chapter {
            gap: 18px;
        }

        .chapter-key-areas {
            /* height: 30vh; */
            justify-content: space-between;
        }

        .in-chapter-cards {
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            gap: 18px;
            width: 100%;
        }

        .in-chapter-cards > :global(*) {
            flex: 0 0 calc((93% - 18px) / 2); /* 2 columns */
            min-width: 0;
        }

        @media (min-width: 1400px) {
            .in-chapter-cards {
                flex-wrap: nowrap; /* force single row */
            }

            .in-chapter-cards > :global(*) {
                flex: 1 1 0; /* equal widths across the row */
                min-width: 0;
            }
        }

        .intro-grid {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 48px;
            padding: 48px 0;
        }

        .intro-grid .chapter {
            max-width: 50vw;
        }

        .intro-grid .contact {
            justify-self: end;
            align-self: flex-end;
            /* min-width: 480px; */
        }

        .intro-grid .contact .in-chapter {
            gap: 12px;
        }

        .content {
            gap: 96px;
            margin-bottom: 96px;
        }

        .more-about-wrap {
            align-self: flex-start;
        }

        .more-about-wrap :global(.button-main){
            min-width: 0px;
        }
    }
</style>
