<style>
.container {
  text-align: center;
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

.container p {
  font-size: 16px;
  line-height: 22px;
  color: rgb(31, 27, 27);
  margin: 0;
}

</style>

<svelte:head>
	<title>SvelteIonic About Page</title>
</svelte:head>

<div class="container">
<h1>About svelteionic</h1>

<p>
	This is the svelteionic project created by Debaditya Malakar to help anyone get started with ionic and svelte for building hybrid apps.
  <br/>
  Make sure to change the appID in the capacitor.config.json
	<br/>
	Use the ionic components as follows: &lt;ion-component-name&gt;&lt;/ion-component-name&gt;
	<br/>
	This template comes with FontAwesomeIcons pre-installed so no need to use Ionicons
	<br/>
	In case you want to modify or remove the navbar pls look into the src/components/Nav.svelte and src/routes/_layout.svelte files;
	<br/>
	The css files for the navbar are present in the static folder
  <br/>
  Make sure to set the set Android Gradle Plugin Version as 3.6.1 and Gradle version as 6.2.1 in the Project Structure from the file menu of Android Studio oor your app may not compile.
</p>
</div>