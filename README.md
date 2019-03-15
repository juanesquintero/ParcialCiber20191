**Nombre:**<br>		
Adobe PDF Escape EXE Social Engineering (No JavaScript)<br>
**Modulo:**		<br>
exploit/windows/fileformat/adobe_pdf_embedded_exe_nojs<br>
**Autor:**		<br>
Jeremy Conway <jeremy@sudosecure.net><br>
**Tipo:**<br>
Local<br>
**Publicacion:**<br>
2010-03-29<br>
**Descripcion:**<br>	 Este módulo integra una carga útil Metasploit en un archivo PDF existente en un método no estándar.
			  El PDF resultante se puede enviar a un destino como parte de un ataque de ingeniería social.
			  Esta es una versión modificada de Adobe PDF Embedded EXE Social Engineering "adobe_pdf_embedded_exe.rb".
			  no requiere que JavaScript esté habilitado y no requiere que el .exe esté adjunto al PDF.
			  El .exe está incrustado en el PDF en un método no estándar utilizando HEX codificación.
			  Es un montón de código reutilizado de adobe_pdf_embedded_exe.rb y los otros módulos de PDF.<br>
**Codigo en ruby:**<br>	- https://www.exploit-db.com/exploits/16682			<br>
**Sistema Operativo:**<br> 	- Windows<br>
**Software:**<br>		- Adobe Reader <= v9.3.3 (Windows XP SP3 English)<br>
**Nombre exe:**<br>		- msf.exe<br>
**Nombre pdf:**<br>		- evil.pdf<br>
**Mensaje:**<br>		- To view the encrypted content please tick the "Do not show this message again" box and press Open.<br>


**Instructivo:**<br> 	1. Abrir terminal en la kali linux<br>
			2. Iniciar el metasploit framework con "msfconsole"<br>
			3. Buscar el exlpoit con "search" <br>
			4. Indicar el exploit que se utilizara con "use (modulo_del_exploit)"<br>
			5. Al estar dentro del exloit usar "show info" para mostrar la informacion de este.<br>
			6. Usar el comando "show options" para mostrar las opciones de lanzamiento<br>
			7. Setear los archivos .pdf y .exe si se quieren cambiar los que estan por defecto (evil.pdf y msf.exe)<br>
			8. Mirar que targets tiene el exploit con "show targets"<br>
			9. Setear el target que se usara solo hay 1 entonces correr "set TARGET 0"<br>
			10. Correr el comando "exploit" para correr el exploit configurado<br>
			11. Buscar y enviar el archivo pdf infectado a la maquina victima por medio de la carpeta compartida<br>
			12. Abrir el archivo en la maquina victima con el "Adobe Reader 9.3.3" <br>

**Comentarios:**<br>	El exe no ejecuto, por un problema de privilegios que restringe el Adobe Reader 9.3.3, busque el error 					y mensaje que se muestra en el video, desabilite la seguridad del Adobe per aun asi siguio saliendo el error, 
			aun asi realice todo el procedimiento y el exploit si lo leepero no ejecuta el .exe.<br>

**Error:**<br>		<p>-"this file is set to be launched by this PDF file. This currently disallowed by your system administrator"
			"C:\WINDOWS\system32\cmd.exe"</p><br>





