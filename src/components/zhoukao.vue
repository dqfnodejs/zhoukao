<template>
	<div>
		<button @click='add'>添加新闻</button>
		<div v-show='isShow'>
			标题：<input type="text" id='headline'>
			内容：<input type="text" id='contents'>
		</div>
		<table>
			<tr>
				<td><h1>标题</h1></td>
				<td><h1>内容</h1></td>
			</tr>
			<tr v-for='(i,index) in arr'>
				<td id='one'>{{i.title}}</td>
				<td id='two'>{{i.content}}<button @click='deletes'>删除</button></td>
			</tr>
		</table>
	</div>
</template>
<script>
	export default{
        data(){
            return{
            	isShow:false,
                arr:[]
            }
        },
        created(){
            this.$http.get('http://localhost:3000')
            .then(e=>this.arr=e.body)

            

            
        },
        methods:{
        	add(){
        		this.isShow=!this.isShow
        	},
        	deletes(e){
        		this.$http.get('http://localhost:3100/del',{id:1},{emlateJSON:true})
                
            	
        	}
        }
     }
</script>
<style>
    

</style>