<template>
    <div>
        <div class="tabs">
            <ul class="nav">
                <li v-for="tab in tabs" :key="tab.active" :class="{ 'tab-active': tab.active, 'nav-item': true}">
                    <a href="#" @click="selectTab(tab)" class="nav-link">{{ tab.name }}</a>
                </li>
            </ul>
        </div>
        <div class="tabs-contents p-2 my-2 tab-content">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: "Tab",
    data() {
        return {
            tabs: []
        };
    },
    created() {
        this.tabs = this.$children;
    },
    methods: {
        selectTab(selectedTab) {
            this.tabs.forEach(tab => {
                tab.active = (tab.name == selectedTab.name);
            });
        }
    }
}
</script>

<style scoped>
.tabs-contents {
    height: 250px;
    border: 1px solid transparent;
    border-radius: 5px;
    color: #004085;
    background-color: #cce5ff;
    border-color: #b8daff;
}
.nav-link {
    border: 1px solid transparent;
    border-radius: 5px;
    color: #004085;
    border-color: #b8daff;
}
.nav-item {
    margin-right: 10px;
}
.tab-active {
    border-radius: 5px;
    background-color: #cce5ff;
}
</style>