# cssGenerator
自动根据点击的dom生成css选择器

  `var cssGenerate=function(event){
  var node=event.target;

  var s='';
  var sa=[];
  while (node.parentNode!=null) {
    sa.push(node.id?"#"+node.id:(node.className?"."+node.className:node.nodeName.toLowerCase()));
    node=node.parentNode;
  }

  s=sa.reverse().join(" ");
  console.log(s);
  return s;
}`
