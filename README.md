# Vue_shopProject
基于vue2.x的购物网站项目练习
3.15
脚手架创建项目，public文件夹添加清除默认样式文件
创建通用组件，Footer,MyHeader,引入less样式，安装less less-leader@3
在App.vue中添加Footer,MyHeader组件
创建四个路由组件，Home，Search，Login，Register
安装配置路由，添加router-link跳转，添加router-view展示，配置默认重定向path:'*',redirect:"/home"
给搜索按钮配置编程式导航
methods:{
        goSearch(){
            this.$router.push('/search')
        }
}
配置路由元信息meta,控制Footer组件的显示与隐藏 meta:{show:true},组件通过$route.meta.show访问，在首页和搜索页显示，在登录注册页隐藏
测试路由传递参数，占位符后面加？,params参数可传可不传。
this.$router.push({name:'search',params:{keyword:this.keyword},query:{k:this.keyword.toUpperCase()}})
接收：{{$route.params.keyword}}  {{$route.query.k}}
测试使用路由组件传递props参数，给路由配置
props:($route)=>{
                return {keyword:$route.params.keyword,k:$route.query.k};
}
