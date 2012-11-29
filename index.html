<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8"> 
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"> 

  <title>MTG Life Counter</title> 
  <meta name="viewport" content="width=device-width, initial-scale=1"> 
  <meta name="apple-mobile-web-app-capable" content="yes" /> 
  <meta name="HandheldFriendly" content="True"> 
  <meta name="MobileOptimized" content="320"/> 
  <meta name="apple-mobile-web-app-capable" content="yes"> 
  <meta name="apple-mobile-web-app-status-bar-style" content="black"> 

  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />
  <style type="text/css">
body{ padding: 0; margin: 0; 
/*activate the GPU for compositing each page */
  /*-webkit-transform: translateZ(0) !important;*/
}
#content{ padding: 0; background: #000;}
#mypage{ background: #000;}
.wut{ display: none !important;}
.jqm { float: left; }
.dw{ min-width: 0px !important;}
.dww, .dw, .dwc , .dwwc table{ width: 100%; padding: 0;}
.dw, .dwwl , .dwwc, .dwc{padding: 0 !important; margin: 0 !important;}
.dwc{padding-top: 30px !important;}
.dwl{font-size: 26px; color: #000; background-color: #fff;}
.ui-header .ui-title{ margin-top: 0; margin-bottom: 0; margin-left: auto; margin-right: auto;}
/*.jqm,.dwpm, .dwwo{ background: -moz-linear-gradient(#ffffff 0px, rgba(0, 0, 0, 0) 42%, rgba(0, 0, 0, 0) 58%, #ffffff 100%) repeat scroll 0 0 transparent !important;}
.dwwwoo{ height: 34px; margin-top: 80px; margin-bottom: 77px; border-top: 3px solid #555; border-bottom: 3px solid #555;}*/
.dwcc input{text-align: center;}
.ui-body-d, .ui-overlay-d, body{text-shadow: none !important;}
.ui-overlay-shadow{box-shadow:0 0 0 rgba(0,0,0,1) !important;}
.bolded-text{
  font-size: 48px !important;  
}
  </style>
  <script src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
  <script type="text/javascript">
  Object.size = function(obj) {
    var size = 0, key;
    for (key in obj) {
        if (obj.hasOwnProperty(key)) size++;
    }
    return size;
};
  var players = [];
  var initLife = 20;
  var edhLife = 40;
  var edhResetted = false;
  var timers = [];
  var time = 2400;
  var lastID = 1;

  $(function(){/* document ready */
    addPlayer();
    addPlayer();
    $( "#newGame" ).bind('tap', reset);
    $( "#newGame" ).bind('taphold', resetEDH);
    $( "#addPlayer" ).click( addPlayer);
    $( "#removePlayer" ).click( removePlayer);

  });
  $(document).bind("mobileinit", function(){
    $.extend(  $.mobile , {
      ajaxEnabled: false,
      activeBtnClass: ''
    });
    
  });
  function removePlayer(){
    var player = players.pop();
    if (!player){return;}
    $(player).scroller('destroy').remove();
    resetWidth();
    
  }
  function addPlayer(){
    var player = $("<select data-role='none'></select>");
    $("#content").append(player);
    var output = [];
    player.life = initLife;
    for (var i=-10;i<80;i++){
      if (i == initLife){
        output.push('<option value="'+i+'" selected="selected">'+i+'</option>');
      }else{
        output.push('<option value="'+i+'">'+i+'</option>');
      }
    }
    player.html(output.join(''));
    player = player.scroller({
      preset:'select',
      rows: 5,
      display: 'inline',
      width: 60,
      theme: 'jqm',
      mode: 'mixed',
      inputClass: 'wut',
      onChange: setLabel,
      onStart: startScroll, 
      onMove: moving,
      formatResult: function(a){return (a+"").substr(1);},
      showLabel: true,
    });
  
  
    players.push( player);
    
    resetWidth();
    return player;
  }
  function resetWidth(){
    var newWidth = 100/(players.length);
    $(".jqm").css("width", newWidth+ "%");
  }
  function reset(event, ui){
    if (edhResetted){ edhResetted = false; return}
    $.each(players, function(index, player){
      player.scroller('setValue', ["_"+initLife], true, 0.8);
    });
  }
  function resetEDH(event, ui){
    edhResetted = true;
    $.each(players, function(index, player){
      player.scroller('setValue', ["_"+edhLife], true, 0.8);
    });
  }
  function setLabel(value, inst, that, that2){
    
    //$('.dwl').html("");
  }
  function startScroll(scroller, val){
    //console.log(Object.size(timers));
    //$(scroller).find('.dwl').html("scrolling");
  }
  function moving(val){
    if (!this.uniqueID){ 
      if (!$(this).attr('id')){ return;} 
      this.uniqueID = $(this).attr('id');
    }
    if (!timers[this.uniqueID] || !timers[this.uniqueID].timer){
      // setting up crappy timers to make the +/- number above scroller appear/hide
      timers[this.uniqueID] = {};
      timers[this.uniqueID].val = val;
      timers[this.uniqueID].timer = true;
    }else{
      clearTimeout(timers[this.uniqueID].timer );
    }
    var ref = $(this).parent().parent().find('.dwl');
    var that = this;
    timers[this.uniqueID].timer = setTimeout(function(){ref.html(""); timers[that.uniqueID].timer = false;}, time);
    var newValue = Math.round(val-timers[this.uniqueID].val);
    if (newValue>0){newValue = "+"+newValue;}
    if (timers[this.uniqueID].lastval != newValue){
      // only update bolding if we have to
	    $(this).parent().parent().find('.dwl').html(newValue);
	    var lastVal = timers[this.uniqueID].realVal -10;
	    timers[this.uniqueID].lastval = newValue;
	    //console.log(Math.round(lastVal));
      $(this).find('li[data-val="_'+Math.round(lastVal)+'"]').removeClass('bolded-text');
      $(this).find('li[data-val="_'+Math.round(val-10)+'"]').addClass('bolded-text');
	    timers[this.uniqueID].realVal = val;
    }
  }
  </script>
  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>
	<link href="css/mobiscroll-2.0.custom.min.css" rel="stylesheet" type="text/css" />
	<script src="js/mobiscroll.core-2.0.js" type="text/javascript"></script>
	<script src="js/mobiscroll.datetime-2.0.js" type="text/javascript"></script>
	<script src="js/mobiscroll.ios-2.0.js" type="text/javascript"></script>
	<script src="js/mobiscroll.jqm-2.0.js" type="text/javascript"></script>
	<script src="js/mobiscroll.select-2.0.js" type="text/javascript"></script>
	<script src="js/mobiscroll.android-2.0.js" type="text/javascript"></script>
	<script src="js/mobiscroll.android-ics-2.0.js" type="text/javascript"></script>
  <script type="text/javascript">

  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'UA-30228091-1']);
  _gaq.push(['_setDomainName', 'abielinski.com']);
  _gaq.push(['_trackPageview']);

  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();

</script>
</head>
<body>
<div data-role="page" id="mypage" style='-moz-user-select: none;-webkit-user-select: none;' onselectstart='return false;'>
  <div data-role="header" data-theme="b">
    <h3>Magically: MTG life counter</h3>
	</div><!-- /header -->
  <div id='main'>
    <div data-role="content" id="content">
    </div>
    <div id="footer" data-role="footer" data-id="footer" data-position="fixed" data-tap-toggle="false" >
        <div data-role="navbar">
          <ul>
            <li><a data-icon="refresh" id="newGame">New Game</a></li>
            <li><a data-icon="plus" id="addPlayer">Add Player</a></li>
            <li><a data-icon="minus" id="removePlayer">Remove Player</a></li>
          </ul>
        </div><!-- /navbar -->
        
		</div>
  </div>
</div>
</body >
</html>
