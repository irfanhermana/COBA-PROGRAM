<?php
      function get_menu($data, $parent = 0) {
	      static $i = 1;
	      $tab = str_repeat(" ", $i);
	      if ($data[$parent]) {
		      $html = "$tab<ul class='sf-menu'>";
		      $i++;
		      foreach ($data[$parent] as $v) {
		      	   $child = get_menu($data, $v->id);
			       $html .= "$tab<li>";
			       $html .= '<a href="'.$v->url_menu.'"'.' '.$v->event.'><img src="'.$v->img_menu.'" width="24" height="24">&nbsp;'.$v->nama_menu.'</a>';     // url -> onclick="return confirm('Anda memilih keluar?')"
			       if ($child) {
				       $i--;
				       $html .= $child;
				       $html .= "$tab";
			       }
			       $html .= '</li>';
		      }
		      $html .= "$tab</ul>";
		      return $html;
	      }
        else {
		      return false;
	      }
      }
session_start();
if($_SESSION[leveluser]=='A'){
      $result = mysql_query("SELECT * FROM menutoko ORDER BY od_menu");
      while ($row = mysql_fetch_object($result)) {
	       $data[$row->id_menu][] = $row;
//	       echo $row;
      }
      $menu = get_menu($data);
      echo "$menu";
}else{
	  $result = mysql_query("SELECT * FROM menutoko WHERE level_menu='AU' ORDER BY od_menu");
      while ($row = mysql_fetch_object($result)) {
	       $data[$row->id_menu][] = $row;
//	       echo $row;
      }
      $menu = get_menu($data);
      echo "$menu";
}
    ?>
