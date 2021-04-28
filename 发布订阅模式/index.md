# 块级作用域
### js 发布订阅模式简单dmeo
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
            // if(this.funcs.indexOf(func) < 0){
            //     console.log("没有订阅该事件");
            // };

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

    // function thePublish(info){
    //     console.log("发布了消息：" + info);
    // };

    ps.listen("theSubscribe", theSubscribe);

    ps.listen("theSubscribe", theSubscribe);

    ps.listen("theSubscribe", theSubscribe);

    ps.listen("theSubscribe", theSubscribe2);

    console.log(ps);

    function triggerPublish(){
        ps.trigger("theSubscribe", "111");

        // ps.trigger(theSubscribe2, "222");

    };