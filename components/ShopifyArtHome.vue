<template>
    <div>
        <div :id="componentId" class="p-16"></div>
        <NuxtLink
            to="/art"
            class="text-5xl hover:text-red-300 animate-pulse py-4"
            >see more</NuxtLink
        >
    </div>
</template>

<script setup>
import { onMounted, ref } from "vue";

// Unique ID for the collection component
const componentId = ref("collection-component-1731794856008");

onMounted(() => {
    if (process.client) {
        const scriptURL =
            "https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js";

        function loadScript() {
            return new Promise((resolve) => {
                const script = document.createElement("script");
                script.async = true;
                script.src = scriptURL;
                script.onload = resolve;
                document.head.appendChild(script);
            });
        }

        function ShopifyBuyInit() {
            const client = ShopifyBuy.buildClient({
                domain: "kmrnv1-si.myshopify.com",
                storefrontAccessToken: "e2de4dbb5c3762e3e93842514874d0e9",
            });

            ShopifyBuy.UI.onReady(client).then((ui) => {
                ui.createComponent("collection", {
                    id: "438430466284", // Collection ID from your Shopify store
                    node: document.getElementById(componentId.value),
                    moneyFormat: "%24%7B%7Bamount%7D%7D",
                    options: {
                        product: {
                            styles: {
                                product: {
                                    "@media (min-width: 601px)": {
                                        "max-width": "calc(33.33333% - 30px)",
                                        "margin-left": "30px",
                                        "margin-bottom": "50px",
                                        width: "calc(33.33333% - 30px)",
                                    },
                                    img: {
                                        height: "calc(100% - 15px)",
                                        position: "absolute",
                                        left: "0",
                                        right: "0",
                                        top: "0",
                                    },
                                    imgWrapper: {
                                        "padding-top": "calc(75% + 15px)",
                                        position: "relative",
                                        height: "0",
                                    },
                                },
                                button: {
                                    ":hover": {
                                        "background-color": "#000000",
                                    },
                                    "background-color": "#000000",
                                    ":focus": {
                                        "background-color": "#000000",
                                    },
                                },
                            },
                            buttonDestination: "modal",
                            contents: {
                                options: false,
                            },
                            text: {
                                button: "View product",
                            },
                        },
                        productSet: {
                            styles: {
                                products: {
                                    "@media (min-width: 601px)": {
                                        "margin-left": "-30px",
                                    },
                                },
                            },
                        },
                        modalProduct: {
                            contents: {
                                img: false,
                                imgWithCarousel: true,
                                button: false,
                                buttonWithQuantity: true,
                            },
                            styles: {
                                product: {
                                    "@media (min-width: 601px)": {
                                        "max-width": "100%",
                                        "margin-left": "0px",
                                        "margin-bottom": "0px",
                                    },
                                },
                                button: {
                                    ":hover": {
                                        "background-color": "#000000",
                                    },
                                    "background-color": "#000000",
                                    ":focus": {
                                        "background-color": "#000000",
                                    },
                                },
                            },
                            text: {
                                button: "Add to cart",
                            },
                        },
                        option: {},
                        cart: {
                            styles: {
                                button: {
                                    ":hover": {
                                        "background-color": "#000000",
                                    },
                                    "background-color": "#000000",
                                    ":focus": {
                                        "background-color": "#000000",
                                    },
                                },
                            },
                            text: {
                                total: "Subtotal",
                                button: "Checkout",
                            },
                            popup: false,
                        },
                        toggle: {
                            styles: {
                                toggle: {
                                    "background-color": "#000000",
                                    ":hover": {
                                        "background-color": "#000000",
                                    },
                                    ":focus": {
                                        "background-color": "#000000",
                                    },
                                },
                            },
                        },
                    },
                });
            });
        }

        // Load the Shopify script and initialize the collection component
        if (window.ShopifyBuy?.UI) {
            ShopifyBuyInit();
        } else {
            loadScript().then(ShopifyBuyInit);
        }
    }
});
</script>
