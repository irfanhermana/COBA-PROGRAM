<html>
  <head>
<link type="text/css" href="casa/index.css" rel="stylesheet" />
<script language="javascript">
function valid(form)
{
  if (form.idanda.value == "")
  {
    alert("Anda belum mengisikan ID.");
    form.idanda.focus();
    return (false);
  }

  if (form.katakunci.value == "")
  {
    alert("Anda belum mengisikan Kata kunci.");
    form.katakunci.focus();
    return (false);
  }
  return (true);
}
</script>
  </head>
    <body>
    <div id="kotaklogin">
        <form name="form" action="ceksan.php" method="post" onSubmit="return valid(this)">
		<div class="kotakloginh">
                     
            				<b>	TOKO CONTOH-TA.COM
            				<?php 
            				include "cfg/konfigurasi.php";
							$querytk=mysql_query("SELECT * FROM toko");
                            $ntk=mysql_fetch_row($querytk); 
							echo $ntk[0]; ?>  </b>		</div>
		<div class="kotakloginb"><center>
						<table border="0">
                				<tr><td align="left" align="center">ID. User</td><td align="right"><input name="idanda" type="text" value="" maxlenght="20" size="20"></td></tr>
			    				<tr><td align="left" align="center">Kata kunci</td><td align="right"><input name="katakunci" type="password" value="" size="20"></td></tr>
			    				<tr><td colspan="2" align="right"><input type="submit" value="Masuk"></td></tr>
    					</table></center>
	  </form>
			
</div></div>
<center><font face="Consolas" size="1">www.contoh-ta.com</font></center>
<?php

switch((isset($_GET['aks'])? $_GET['aks']:''))
{

default: 
echo "<script language=\"javascript\">
    		alert(\"Semoga Alloh membukakan pintu rezeki yang barokah. Amin\");
   		  </script>";
break;

case "error1":
echo "<script language=\"javascript\">
    		alert(\"Terjadi kesalahan, periksa kembali ID dan KATA KUNCI Anda!.\");
   		  </script>";
break;

case "mess2":
	echo "<script language=\"javascript\">
    		alert(\"Anda sudah keluar dari program toko.\");
   		  </script>";
break;

case "error3":
	echo "<script language=\"javascript\">
    		alert(\"Tidak bisa di akses tanpa login!\");
   		  </script>";
break;

case "error4":
	echo "<script language=\"javascript\">
    		alert(\"JAYADIN GANTENG!\");
   		  </script>";
break;
}
?>
  </body>
</html>
