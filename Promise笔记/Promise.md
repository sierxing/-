# Promise

## 一、Promise初体验

```html
<button id="btn">按钮</button>

    <script>
        function rand(m,n){
            return Math.ceil(Math.random() * (n-m+1)) + m-1;
        }
        const btn = document.querySelector('#btn');

        btn.addEventListener('click',function(){
            const p = new Promise((resolve,reject)=>{
            setTimeout(() => {
                let n = rand(1,100);
                if(n<=30){
                    resolve(n);
                }else {
                    reject(n);
                 }
             },200);
        });
      
            p.then((value) => { 
                alert("恭喜获奖" + value);
            },(reason)=>{
                alert("再接再厉" + reason);
            });
        })
    </script>
```
