<script lang="ts">
    import Button from "$lib/components/Buttons/Button.svelte";
    import ButtonSmall from "./Buttons/ButtonSmall.svelte";
</script>

<footer class="footer">
    <!-- Top copy -->
    <div class="top">
        <div class="project-headline">Message me</div>
        <div class="sub-headline">
            If you want to work together. <br /> If you have any questions.
            <br /> If you just want to chat.
        </div>
    </div>

    <div class="button-wrapper">
        <Button href="mailto:vivien.serve@gmail.com" type="external">
            mail me: vivien.serve@gmail.com
        </Button>
    </div>

    <div class="divider"></div>

    <div class="info-grid">
        <div class="row-group">
            <div class="row">
                <div class="table-label">SOCIAL</div>
                <div class="value">
                    <ButtonSmall
                        href="https://www.linkedin.com/in/vivien-serve-25aa4a17a/?originalSubdomain=de"
                        type="external"
                    >
                        LinkedIn
                    </ButtonSmall>
                </div>
            </div>

            <div class="row">
                <div class="table-label">LOCATION</div>
                <div class="table-value">Beautiful Potsdam, Germany</div>
            </div>
        </div>

        <div class="divider"></div>

        <div class="row-group">
            <div class="row">
                <div class="table-label">PAGES</div>
                <div class="value stack">
                    <ButtonSmall href="/" type="internal">Works</ButtonSmall>
                    <ButtonSmall href="/about" type="internal"
                        >About</ButtonSmall
                    >
                </div>
            </div>

            <div class="row">
                <div class="table-label">Must haves</div>
                <div class="value stack">
                    <ButtonSmall href="/" type="internal"
                        >Legal Notice</ButtonSmall
                    >
                    <ButtonSmall href="/about" type="internal"
                        >Privacy</ButtonSmall
                    >
                </div>
            </div>
        </div>

        <div class="divider"></div>

        <div class="row">
            <div class="table-label">production</div>
            <div class="table-value">Vivien Serve</div>
        </div>

        <div class="divider"></div>
    </div>
</footer>

<style>
    .footer {
        padding: 24px 16px 16px 16px; /* mobile */
        background: var(--color-primary);
        color: #ffffff;
    }

    .footer :global(.button-main) {
        color: var(--color-highlight-footer);
        border-color: var(--color-highlight-footer);
    }

    .footer :global(.button-main:hover) {
        color: var(--color-primary);
    }

    .footer :global(.button-small) {
        color: var(--color-highlight-footer);
        border-color: var(--color-highlight-footer);
    }

    .button-wrapper {
        padding-bottom: 16px;
    }

    .table-label {
        color: #ffffff;
    }

    .table-value {
        color: #ffffff;
    }

    .project-headline {
        color: #ffffff;
        padding-bottom: 16px;
    }

    .top {
        margin-bottom: 156px;
    }

    .sub-headline {
        color: #ffffff;
    }

    .info-grid {
        display: flex;
        flex-direction: column;
        gap: 16px;
        padding-top: 16px;
    }

    .row {
        display: grid;
        grid-template-columns: 140px 1fr;
        row-gap: 0px;
    }

    .value {
        min-width: 0;
    }

    .stack {
        display: grid;
        gap: 0px;
    }

    .divider {
        height: 1px;
        background: #ffffff; /* white divider */
        margin: 0px 0;
    }

    @media (min-width: 900px) {
        .footer {
            padding: 48px;
        }

        .project-headline {
            padding-bottom: 24px;
        }

        .stack {
            gap: 2px;
        }

        .info-grid {
            flex-direction: row;
            justify-content: space-between;
        }

        .row-group {
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .button-wrapper {
            display: flex;
            justify-content: flex-end; 
            padding-bottom: 16px;
        }

        .top {
            margin-bottom: 244px;
        }
    }
</style>
