Yii2 TCPDF
==========

Yii2 TCPDF to load TCPDF libraries in a Yii2 site

<h2>CHANGELOG</h2>

<ul>
  <li>0.3 - Added example</li>	
  <li>0.2 - Loaded tcpdf_6_0_075</li>
  <li>0.1 - Initial Releases</li>
</ul>

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
$ php composer.phar require cinghie/yii2-tcpdf "dev-master"
```

or add

```
"cinghie/yii2-tcpdf": "dev-master"
```

to the ```require``` section of your `composer.json` file.

## CONFIGURATION

<ul>
	<li>Add in your configuration file, in component section:
		<pre>'component' => [ 
...
		// Yii2 TCPDF
		'tcpdf' => [
			'class' => 'cinghie\tcpdf\TCPDF',
		],
		...
]</pre>
	</li>
	<li>Add in your SiteController the action:
		public function actionTcpdf()
    {
		return $this->render('tcpdf');
	}
	</li>
	<li>Add in your view/site folder the file tcpdf.php from example folder</li>
	<li>Now you can view the example at the links: 
		<ul>
			<li>Simple URL: index.php?r=site/tcpdf</li>
			<li>Pretty URL: site/tcpdf</li>
		</ul>
	</li>
	<li>To insert TCPDF in your extension you must only:
		<ul>
			<li>// Load Component Yii2 TCPDF 
\Yii::$app->get('tcpdf');</li>
			<li>// Close Yii2
\Yii::$app->end();</li>
		</ul>
	</li>
</ul>