
Nombre:			- Adobe PDF Escape EXE Social Engineering (No JavaScript)
Modulo			- exploit/windows/fileformat/adobe_pdf_embedded_exe_nojs
Autor:			- Jeremy Conway <jeremy@sudosecure.net>
Tipo:			- Local
Publicacion:		- 2010-03-29
Descripcion:		- Este módulo integra una carga útil Metasploit en un archivo PDF existente en un método no estándar.
			  El PDF resultante se puede enviar a un destino como parte de un ataque de ingeniería social.
			  Esta es una versión modificada de Adobe PDF Embedded EXE Social Engineering "adobe_pdf_embedded_exe.rb".
			  no requiere que JavaScript esté habilitado y no requiere que el .exe esté adjunto al PDF.
			  El .exe está incrustado en el PDF en un método no estándar utilizando HEX codificación.
			  Es un montón de código reutilizado de adobe_pdf_embedded_exe.rb y los otros módulos de PDF.

Codigo en ruby:		- https://www.exploit-db.com/exploits/16682			
Vulnerabilidad:		-
Sistema Operativo: 	- Windows
Software:		- Adobe Reader <= v9.3.3 (Windows XP SP3 English)
Nombre exe:		- msf.exe
Nombre pdf:		- evil.pdf
Mensaje:		- To view the encrypted content please tick the "Do not show this message again" box and press Open.


Instructivo:		1. Abrir consonal en la kali linux
			2. Iniciar el metasploit con "msfconsole"
			3. Indicar el exploit que se utilizara con "use (modulo_del_exploit)"
			4. Al estar dentro del exloit usar "show info" para mostrar la informacion de este.
			5. Usar el comando "show options" para mostrar las opciones de lanzamiento
			6. 
			7.
			8. 


