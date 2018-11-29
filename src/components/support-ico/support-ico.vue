<template>
	<span class="support-ico" :span="iconCls"></span>
</template>

<script>
	export default{
		name:  'support-ico',
		props: {
			size:{
				type: Number,
			},
			type:{
				type: Number
			}
		},
		computed: {
			iconCls(){
				const classMap = ['decrease','discount','special','invoice','guarantee']
				return `icon-${this.size} ${classMap[this.type]}`
			}
		}
	}
</script>

<style lang="stylus" scoped>
		@import "~common/stylus/mixin"
		@import "~common/stylus/variable"
		
		.support-ico
		  display: inline-block
		  background-repeat: no-repeat		
</style>