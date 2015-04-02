# cakephpapicallguide

1. Use create Behavior to call remote api by using HttpSocket

```
function getCategoriesFromAPI(){

	// for example
	$results = $HttpSocket->get('http://www.google.com/search', 'q=cakephp');
	return $result;
}

```

2. Use that Behavior in model

```

var $actsAs = array('MyRemoteAPI');

```

[Reference for Behaviors](http://book.cakephp.org/1.3/en/The-Manual/Developing-with-CakePHP/Behaviors.html)

3. Stop using existing model functions/methods, use the ones in Behavior instead

```

$data = $this->Category->getCategoriesFromAPI();

```
 