<template>
    <div class="container">
        <h1>Atlas: The Ultimate Guide to the World</h1>
        <div class="header">
            <p class="text">
                Atlas is a website that lists every country
                with their flags and facts. You can explore
                the world map, search by name or region,
                and filter by criteria.
                Learn about the world and its diversity
                with Atlas!
            </p>
            <div class="main-button">
                <span class="filter">Filter</span>
                <button class="region-button">
                    <span class="region">Region</span>
                    <img src="src/assets/svg/fi-ss-angle-small-down.svg">
                </button>
            </div>
        </div>
        <ul>

            <slot />
        </ul>
    </div>
</template>

<style scoped>
ul {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    /* background-color: red; */
}

.container {
    background-color: #A7B3C7;
    ;
    width: 1320px;
    margin: auto
}

h1 {
    font-family: Inter;
    font-size: 30px;
    font-weight: 600;
    color: black;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.text {
    font-family: Inter;
    font-size: 16px;
    font-weight: 400;
    color: #000000B2;
    flex-basis: 62%;
}

.main-button {
    display: flex;
    align-items: center;
    background-color: rgba(225, 225, 225, 0.5);
    border-radius: 30px;
    padding: 4px 4px 4px 16px;
    gap: 10px
}

.filter {
    font-family: Inter;
    font-size: 14px;
    font-weight: 500;
    color: black;
}

.region-button {
    display: flex;
    align-items: center;
    border: none;
    background-color: white;
    border-radius: 30px;
    padding: 8px 16px;
    gap: 5px
}

.region {
    font-family: Inter;
    font-size: 14px;
    font-weight: 500;
    color: black;


}
</style>