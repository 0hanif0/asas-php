# ASAS PHP (PHP: Hypertext Preprocessor)

### HTML,CSS,Javascript adalah Client Side
### PHP adalah Server Side
### Webserver - XAMPP,Laragon


## Variable
```php
<?php
  $Nama = 'Hanif'; //string
  $Umur = 18; //integer
  $berat = 99.9; //float
  $student = true; //boolean
  echo "Nama $Nama"; // -- Nama Hanif -- double quote display value variable
  echo 'Nama $nama'; // -- Nama $nama -- single quote display text
?>
```

## Comment
```php
<?php
  // komen satu baris
  
  /* komen banyak baris */
?>
```

## php in html
```php
<html>
<h1>Selamat pagi
<?php echo $nama; ?>
</h1>
</html>
```

## Array
```php
<?php
  $student = []; //array kosong
  $student = ['ali','abu']; //array ada nilai awal
  $student[] = 'amin'; //ubah array di hujung
  $student[2] = 'ikram'; //ubah nilai item dalam array
  var_dump($student); //untuk melihat kandungan array
  print_r($student); //untuk melihat kandungan array
?>
```

### Associative Array
### Nested Array

## Logic
### if-elseif-else
```php
<?php
 if ($nama == 'Hanif') {
 echo "Selamat Datang Hanif";
 } elseif ($nama == 'Raju') {
 echo "Apa Khabar Raju";
 } else {
 echo "Saya PHP. Awak siapa?";
 }
?>
```

### switch-case
```php
<?php
 switch($nama) {
 case 'Hanif':
 echo "Selamat Datang Hanif"; break;
 case 'Raju':
 echo "Apa Khabar Raju"; break;
 default:
 echo "Saya PHP. Awak siapa?";
 }
?>
```

## Operator
### matematik
```php
<?php
 $x = 15 - 4; // tolak, hasil 11
 $x = 15 + 4; // tambah, hasil 19
 $x = 15 / 4; // bahagi, hasil 3.75
 $x = 15 * 4; // darab, hasil 60
 $x = 15 % 4; // modulus (baki), hasil 3
 $x = 15 ** 4; // kuasa, hasil 50,625
?>
```

### assignment
```php
<?php
 $x = 15; // memberi nilai 15
 $x += 15; // ditambah 15
 $x -= 15; // ditolak 15
 $x *= 15; // didarab
 $x /= 15; // dibahagi 15
 $x %= 15; // operasi modulus
 
 $x++; // memberi nilai, kemudian ditambah 1
 ++$x; // ditambah 1, kemudian memberikan nilai
 $x--; // memberi nilai, kemudian ditolak 1
 --$x; // ditolak 1, kemudian memberikan nilai
?>
```

### pembandingan
```php
<?php
($x == $y)  // sama dengan
($x === $y)  // sama dengan, dan membandingkan data type sekali
($x != $y)  // tidak sama dengan
($x !== $y)  // tidak sama dengan, dan membandingkan data type sekali
($x > $y)  // lebih besar
($x >= $y)  // lebih besar atau sama dengan
($x < $y)  // lebih kecil
($x <= $y)  // lebih kecil atau sama dengan
?>
```

## Loop
### for
```php
<?php
 for($x = 0; $x < 10; $x++) {
 echo "$x <br>";
 }
?>
```

### for each
```php
<?php
 $kelas = [];
 $kelas[] = ['nama' => 'Hanif','umur' => 18];
 $kelas[] = ['nama' => 'Ali','umur' => 20];
 foreach($kelas as $murid) {
 echo $murid['nama'];
 echo $murid['umur'];
 }
?>
```

### while
```php
<?php
 $a = 0;
 while($a < 10) {
 echo "$a <br>";
 $a++;
 }
?>
```

### do while
```php
<?php
 $a = 0;
 do {
 echo "$a <br>";
 $a++;
 } while($a < 10);
?>
```

## Function
```php
<?php
 function tambah ( $a, $b ) {
 return $a + $b;
 }
 echo tambah(4, 6);
?>
```

## Include & Require
```php
//include() membenarkan fail dipanggil, walaupun terdapat ralat dalam kod, tapi akan ada WARNING
//require() tidak membenarkan fail dengan ralat untuk dipanggil, akan ada ERROR
<?php
include('functions.php');
// fungsi daripada functions.php
echo tambah(6, 4);
?>
```

## Superglobals
- $GLOBALS
- $_SERVER
- $_REQUEST
- $_POST
- $_GET
- $_FILES
- $_ENV
- $_COOKIE
- $_SESSION
