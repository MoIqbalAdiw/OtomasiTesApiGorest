"# OtomasiTesApiGorest" 
Object API test :
https://gorest.co.in/public/v2/users

Tools yang dipakai :
Language = Java
Framework Testing = JUnit
Testing Library = RestAssured, AssertJ-Core, Cucumber

package pendukung : (dalam src>test>java>)
features : 
api.feature = berisi skenario pengujian dalam format Gherkin
helper :
package JSONSchemaData = berisi format/skema standard JSON sebagai acuan validasi format JSON dalam test
EndPoint.java = berisi referensi alamat web yang akan dipakai untuk eksekusi test
Models.java = berisi kode untuk request (RestAssured) berbagai support beberapa langkah dalam test, seperti setup header, get, post, delete, patch.
Utility.java = berisi kode support beberapa hal lain dalam test, seperti untuk mendapatkan kembalian objek File JSON Schema, dan untuk fungsi pembuatan random email sebagai value alamat email yang dipakai saat test pst create user
pages :
ApiPage.java = berisi beberapa fungsi mendapatkan respon atas beberapa request pada file Models.java serta melakukan assertion atasnya.
runner :
ApiRunner.java = sebagai runner untuk memerintahkan JUnit untuk menggunakan Cucumber runner, acuan kkode memberi rujukan package file step test dan lokasi file features
stepDef :
ApiStep.java = sebagai file rujukan langsung dari file api.feature, menjabarkan fungsi yang harus dijalankan pada setiap annotation sesuai step di api.feature

