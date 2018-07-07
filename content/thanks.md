---
title: thanks
---

These lovely people have contributed a fix to my blog. If you want to see yourself in this list, send me a pull request! Every post in my blog has an edit link (the octocat button) that lets you edit the blog post directly in the browser which automatically sends me a pull request.

Or [visit my repository](https://github.com/ghuntley/ghuntley) and send me a pull
request the old fashioned way.

<div class="contributors"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

<script>
  $.when(
    $.ajax('https://api.github.com/repos/reactiveui/website/contributors?per_page=250'),
    $.ajax('https://api.github.com/repos/reactiveui/reactiveui/contributors?per_page=250'))
  .then(function(websiteData, reactiveUIData) {
    var persons = {};
    var allData = websiteData[0].concat(reactiveUIData[0]);

    for(var i = 0; i < allData.length; i++) {
        persons[allData[i].login] = allData[i];
    }

    var sortedLogins = Object.keys(persons).sort();

    $(sortedLogins).each(function (index, login) {
      var person = persons[login];
      var img = '<img class="contributor" src="' + person.avatar_url + '" />';
      $('.contributors')
        .append('<a class="contributor-name" title="' + person.login + '" href="' + person.html_url + '">' 
                + img + '</a>');
    });
  });
</script>

<style>
 
  #content img {
    width: 48px;
    margin: 5px 5px;
    display: inline-block;
  }
  .contributor {
    border-radius: 730px;
    margin: 10px 10px 0 0;
  }

  .contributor-name {
    border-bottom: none;
  }
</style>
