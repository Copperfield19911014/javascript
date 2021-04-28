# js 发布订阅模式简单dmeo
---
    class PublishSubscribe{
        constructor(){}
        funcs = {};
        listen(type, fn){
            if(!(type in this.funcs)){
                console.log("没有订阅该事件");
                this.funcs[type] = [];
            }

            this.funcs[type].push(fn);
        }

        trigger(type, params){

            this.funcs[type].forEach(event => {
                event(params);
            })

        }
    };


    let ps = new PublishSubscribe();

    function theSubscribe(params){
        console.log("给" + params + "发送了消息");
    };

    function theSubscribe2(params){
        console.log(params + "您好！！！");
    }

    /*订阅消息
    ps.listen("theSubscribe", theSubscribe);

    ps.listen("theSubscribe", theSubscribe);

    ps.listen("theSubscribe", theSubscribe);

    ps.listen("theSubscribe", theSubscribe2);
    */

    //发布消息事件
    function triggerPublish(){
        ps.trigger("theSubscribe", "111");

    };