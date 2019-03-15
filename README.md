
**Nombre:**		- Adobe PDF Escape EXE Social Engineering (No JavaScript)
**Modulo:**			- exploit/windows/fileformat/adobe_pdf_embedded_exe_nojs
**Autor:**			- Jeremy Conway <jeremy@sudosecure.net>
**Tipo:**			- Local
**Publicacion:**		- 2010-03-29
**Descripcion:**		- Este módulo integra una carga útil Metasploit en un archivo PDF existente en un método no estándar.
			  El PDF resultante se puede enviar a un destino como parte de un ataque de ingeniería social.
			  Esta es una versión modificada de Adobe PDF Embedded EXE Social Engineering "adobe_pdf_embedded_exe.rb".
			  no requiere que JavaScript esté habilitado y no requiere que el .exe esté adjunto al PDF.
			  El .exe está incrustado en el PDF en un método no estándar utilizando HEX codificación.
			  Es un montón de código reutilizado de adobe_pdf_embedded_exe.rb y los otros módulos de PDF.

**Codigo en ruby:**		- https://www.exploit-db.com/exploits/16682			
**Sistema Operativo:** 	- Windows
**Software:**		- Adobe Reader <= v9.3.3 (Windows XP SP3 English)
**Nombre exe:**		- msf.exe
**Nombre pdf:**		- evil.pdf
**Mensaje:**		- To view the encrypted content please tick the "Do not show this message again" box and press Open.


**Instructivo:** 1. Abrir terminal en la kali linux
 2. Iniciar el metasploit framework con "msfconsole"
			3. Buscar el exlpoit con "search" 
			4. Indicar el exploit que se utilizara con "use (modulo_del_exploit)"
			5. Al estar dentro del exloit usar "show info" para mostrar la informacion de este.
			6. Usar el comando "show options" para mostrar las opciones de lanzamiento
			7. Setear los archivos .pdf y .exe si se quieren cambiar los que estan por defecto (evil.pdf y msf.exe)
			8. Mirar que targets tiene el exploit con "show targets"
			9. Setear el target que se usara solo hay 1 entonces correr "set TARGET 0"
			10. Correr el comando "exploit" para correr el exploit configurado
			11. Buscar y enviar el archivo pdf infectado a la maquina victima por medio de la carpeta compartida
			12. Abrir el archivo en la maquina victima con el "Adobe Reader 9.3.3" 

Comentarios:		-El exe no ejecuto, por un problema de privilegios que restringe el Adobe Reader 9.3.3, busque el error o mensaje 
			 que se muestra en el video, desabilite la seguridad del Adobe per aun asi siguio saliendo el error, 
			 aun asi realice todo el procedimiento y el exploit si lo leepero no ejecuta el .exe.

Error:			- "this file is set to be launched by this PDF file. This currently disallowed by your system administrator"
			  "C:\WINDOWS\system32\cmd.exe"





