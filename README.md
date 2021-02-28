<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title></title>
<style>
    .box{
        width: 100px;
        height: 20px;
        padding: 10px;        
        margin-bottom: center;
        border: 2px;
        border-style: solid;
        border-color: green;
    }
</style>
<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
<script>
$(document).ready(function(){
    $("select").change(function(){
        $(this).find("option:selected").each(function(){
            var optionValue = $(this).attr("value");
            if(optionValue){
                $(".box").not("." + optionValue).hide();
                $("." + optionValue).show();
            } else{
                $(".box").hide();
            }
        });
    }).change();
});
</script>
</head>
<body>
    <div>
        <select>
            <option>Choose device</option>
            <option value="a">Sensor</option>
            <option value="b">Motor</option>
            <option value="c">Relay</option>
        </select>
    </div>
    <div class="a box">Sensor ID</div>
    <div class="a box">Sensor Name</div>
    <div class="b box">Motor ID</div>
    <div class="b box">Motor Name</div>
    <div class="c box">Relay id</div>
    <div class="c box">Relay name</div>
    <div class="c box">Modules
<script language="JavaScript" type="text/javascript">

            
            Modules();
            function Modules()
            {
                var Modules = 0
                document.write("<select name='Modules'>");

                for (var i=1; i <=32; i++)
                {
                    Modules++;
                    document.write("<option>" + Modules + "</option>");
                }

            }
   </script>
    </div>
</body>
</html>
