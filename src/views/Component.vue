<template>
    <div id="component">
        <h1 class="py-2 component-head">Alert</h1>
        <div class="px-4">
            <alert type="success">
                <p class="col-11 item-left item-margin p-0 py-2">This is a <strong>success</strong> alert</p>
            </alert>
            <alert type="error">
                <p class="col-11 item-left item-margin p-0 py-2">This is a <strong>error</strong> alert</p>
            </alert>
            <alert type="danger">
                <p class="col-11 item-left item-margin p-0 py-2">This is a <strong>danger</strong> alert</p>
            </alert>
            <alert type="warning">
                <p class="col-11 item-left item-margin p-0 py-2">This is a <strong>warning</strong> alert</p>
            </alert>
        </div>
        <h1 class="py-2 component-head component-tab">Tabs</h1>
        <tabs class="px-4 text-left">
            <tab name="First" :selected="true">
                <p class="item-left">Fusce hendrerit enim pretium, fringilla sapien quis, mattis purus. Suspendisse auctor porttitor pulvinar. Etiam et ipsum laoreet, lacinia quam suscipit, lacinia elit. Sed a rutrum sapien, sed convallis ex. Curabitur nulla massa, aliquam nec pellentesque at, tincidunt quis urna. Suspendisse porttitor sed augue blandit lacinia. Quisque a justo et dolor auctor consequat. Integer finibus suscipit tortor tempus tincidunt. Nam semper purus sit amet eros hendrerit, in elementum sem placerat.</p>
            </tab>
            <tab name="Second">
                <ul class="item-left">
                    <li>Integer vel odio faucibus, feugiat lectus sit amet, sollicitudin risus.</li>
                    <li>Sed id tellus placerat, dignissim mauris eu, euismod mauris.</li>
                    <li>Proin ullamcorper erat et hendrerit volutpat.</li>
                </ul>
            </tab>
            <tab name="Third">
                <alert type="danger">
                    <p class="col-11 item-left item-margin p-0 py-2">This alert contains <strong>html</strong> elements</p>
                </alert>
            </tab>
        </tabs>
    </div>
</template>

<script>
// @ is an alias to /src
import alert from '@/components/Alert.vue'
import tabs from '@/components/Tabs.vue'
import tab from '@/components/Tab.vue'

export default {
    name: 'Component',
    components: {
        alert,
        tabs,
        tab
    }
}
</script>

<style scoped>
#component {
    margin: auto;
    border: 1px solid #2c3e50;
    border-radius: 5px;
    width: 80%;
}
.component-head {
    text-align: center;
    border-radius: 5px 5px 0 0;
    border-bottom: 1px solid #2c3e50;
    background-color: #42b983;
}
.component-tab {
    border-radius: 0;
}
.item-margin {
    margin: 0;
}
.item-left {
    text-align: left;
}
.test {
    border: 1px solid #2c3e50;
}
@media (max-width: 960px) {
    #component {
        width: 100%;
    }
}
</style>
