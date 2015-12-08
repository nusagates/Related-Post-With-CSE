This simple repository is created for everyone who want add custom related post with Google Custom Search Engine (CSE). How to create related post with CSE will be described bellow:
<h2>How To Create Related Post with Google CSE</h2>
<ol>
<li>Paste codes below before ending of head tag &lt;&#47;head&gt;<br/><br/>
<code>
&lt;script src='http://www.google.com/jsapi' type='text/javascript'>&lt;&#47;script&gt;
&lt;script type='text/javascript'>
google.load('search', '1', {language: 'in', style: google.loader.themes.V2_DEFAULT});
google.setOnLoadCallback(function() {
  var customSearchOptions = {};
  var imageSearchOptions = {};
  imageSearchOptions['layout'] = 'google.search.ImageSearch.LAYOUT_POPUP';
  customSearchOptions['enableImageSearch'] = true;
  var customSearchControl =   new google.search.CustomSearchControl('<b>partner-pub-8648292563278695:5431983969</b>', customSearchOptions);
  customSearchControl.setResultSetSize(google.search.Search.FILTERED_CSE_RESULTSET);
  var options = new google.search.DrawOptions();
  options.enableSearchResultsOnly();
  customSearchControl.draw('cse', options);

    customSearchControl.execute("<data:post.title/>");
  
}, true);
&lt;&#47;script&gt;
</code>
</li>

<li>Paste codes below on the place where you want to display output of related post<br/> <br/>
&lt;h3>Related Post&lt;&#47;h3&gt;<br/>
&lt;div id='cse' style='width: 100%;'&gt;...&lt;&#47;div&gt;
</li>
<li>Do not forget replace <b>partner-pub-8648292563278695:5431983969</b> with your own code. But if you do not have any account, you can skip this step</li>
<li>Save your template</li>
</ol>
