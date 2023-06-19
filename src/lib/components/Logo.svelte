<script lang="ts">
</script>

<a href="/">
    <div class="wrapper">
        <div class="image-wrap">
            <img src="/images/portrait.webp" alt="" />
        </div>
        <span>dnikolov.dev</span>
    </div>
</a>

<style lang="scss">
    .wrapper {
        display: flex;
        align-items: center;
        gap: 2rem;

        span {
            color: white;
            font-size: 1.5rem;
            font-weight: 700;
            position: relative;
            overflow: hidden;

            &::before {
                content: '';
                position: absolute;
                left: 0;
                bottom: 2px;
                height: 2px;
                width: 0;
                background-color: white;
                transition: transform 200ms 200ms ease, width 200ms ease;
                transform: translateX(100%);
            }
            &:hover {
                &::before {
                    width: 100%;
                    transform: translateX(0);
                }
            }

            &::after {
                content: 'dnikolov.dev';
                color: rgb(142, 21, 142);
                position: absolute;
                bottom: -1px;
                left: 1px;
            }
        }
    }
    .image-wrap {
        width: fit-content;
        border-radius: 50%;
        overflow: hidden;
        max-height: 100%;
        outline: 3px solid rgba(128, 0, 128, 0.5);
        img {
            max-width: 80px;
            height: 100%;
            object-fit: contain;
        }
    }
</style>
