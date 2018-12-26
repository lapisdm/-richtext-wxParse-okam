<template>
	<import src="./wxParse/wxParse.axml"/>
	<template is="wxParse" :data="{wxParseData:urlNew.nodes}"/>
</template>
<script>
export default {
    config: {
    },

    props: {
        urlNew: String
    },

    components: {
    },

    data: {
    },
	created(){
		var WxParse = require('./wxParse/wxParse.js');
		var that = this;
		WxParse.wxParse('urlNew', 'html', that.urlNew, that, 5);
	},
    methods: {

    }
};
</script>
<style lang="less">
@import "./wxParse/wxParse.acss";

</style>
