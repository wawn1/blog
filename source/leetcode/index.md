---
title: leetcode
date: 2021-04-07 12:49:25
---
<!-- style="display:flex; justify-content:flex-end; align-items: center;" -->
<div style="overflow: auto;">
    <div style="float: right;">
        <input type='text' class='text' id='filtername' placeholder="Search...">
        <i class="fas fa-search"></i>
    </div>
</div>



<!-- Row Highlight Javascript -->
<script src="https://cdn.bootcdn.net/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script type="text/javascript">
jQuery.expr[':'].contains = function(a, i, m) {
  return jQuery(a).text().toUpperCase()
      .indexOf(m[3].toUpperCase()) >= 0;
};
$(function(){
       $("#filtername").keyup(function(){
	      $("table tbody tr")
					.hide()
					.filter(":contains('"+( $(this).val() )+"')")
					.show();
	   }).keyup();
  })

</script>

<style type="text/css">
table tr td,th{
    border: none;
    border-bottom: 1px solid #f0f0f0;
}
table thead{
    background-color: #fafafa;
}

</style>

|  id  |            title            | category |
| :--: | :-------------------------: | :------: |
| aaa  | {% post_link hello-world %} |    a     |
|  a   |              a              |    a     |
