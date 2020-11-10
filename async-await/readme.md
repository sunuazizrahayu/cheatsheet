v1
```
<script>
async function getData() {
  let data = await fetch('https://jsonplaceholder.typicode.com/posts/1');
  return data;
}


console.log('sebelum');
(async function(){
	console.log('proses');
	let result = await getData();
	console.log(result);
    console.log('sesudah');
})()
</script>
```
