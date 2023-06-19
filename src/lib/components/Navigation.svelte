<script lang="ts">
    import { page } from '$app/stores';
</script>

<nav>
    <ul>
        <li class:current={$page.url.pathname === '/'}><a href="/">Home</a></li>
        <li class:current={$page.url.pathname === '/blog'}><a href="/blog">Blog</a></li>
        <li class:current={$page.url.pathname === '/contact'}>
            <a href="/contact">Get In Touch</a>
        </li>
    </ul>
</nav>

<style lang="scss">
    nav {
        ul {
            display: flex;
            justify-content: flex-end;
            gap: 2rem;

            li {
                isolation: isolate;
            }

            li.current {
                a {
                    position: relative;
                    background-color: purple;
                    border-color: transparent;

                    &:hover {
                        background-color: rgb(153, 0, 153);
                        color: white;
                    }

                    &::before {
                        content: '';
                        position: absolute;
                        background-color: white;
                        width: 100%;
                        height: 100%;
                        top: 3px;
                        left: 3px;
                        z-index: -1;
                    }
                }

                &:nth-child(2) {
                    a {
                        background-color: rgb(255, 208, 0);
                        color: black;

                        &:hover {
                            background-color: rgb(255, 221, 68);
                            color: black;
                        }
                    }
                }

                &:nth-child(3) {
                    a {
                        background-color: rgb(255, 170, 0);
                        color: black;

                        &:hover {
                            background-color: rgb(248, 178, 36);
                            color: black;
                        }
                    }
                }
            }

            a {
                width: max-content;
                display: block;
                border: 1px solid white;
                padding: 0.5rem 2rem;
                color: white;
                transition: all 200ms ease;

                &:hover {
                    background-color: white;
                    color: black;
                }
            }
        }
    }
</style>
