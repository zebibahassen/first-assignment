`Name: Zebiba Hassen
Id: ATR/6348/08
Section: 2
`
# 1. CapitalizeServer.java

 The server program accepts requests from clients to
 capitalize strings.  When clients connect, a new thread is
 started to handle an interactive dialog in which the client
 sends in a string and the server thread sends back the
 capitalized version of the string.
 The program is runs in an infinite loop, so shutdown in platform
 dependent.
 
 MAIN:
     
     Application method to run the server runs in an infinite loop
     listening on port 9898.  When a connection is requested, it
     spawns a new thread to do the servicing and immediately returns
     to listening.  The server keeps a unique client number for each
     client that connects just to show interesting logging
     messages. 
     
 CAPITALIZER:

     A private thread to handle capitalization requests on a particular
     socket.  The client terminates the dialogue by sending a single line
     containing only a period.
     
 RUN:

     Services this thread's client by first sending the
     client a welcome message then repeatedly reading strings
     and sending back the capitalized version of the string.
      
 LOG:

      Logs a simple message.  In this case we just write the
      message to the server applications standard output.
      

CapitalizeClient.java

 A simple Swing-based client for the capitalization server.
 It has a main frame window with a text field for entering
 strings and a textarea to see the results of capitalizing
 them.
 
 
 CAPITALIZECLIENT:

      Constructs the client by laying out the GUI and registering a
      listener with the textfield so that pressing Enter in the
      listener sends the textfield contents to the server.
     
 ACTIONPERFORMED:

      Responds to pressing the enter key in the textfield
      by sending the contents of the text field to the
      server and displaying the response from the server
      in the text area.  If the response is "." we exit
      the whole application, which closes all sockets,
      streams and windows.
            
 CONECTTOSERVER:

      Implements the connection logic by prompting the end user for
      the server's IP address, connecting, setting up streams, and
      consuming the welcome messages from the server.  The Capitalizer
      protocol says that the server sends three lines of text to the
      client immediately after establishing a connection.
     
 MAIN:

      Runs the client application.
---------------------------------------------------------------------



# 2. ADDER JAVA APP

CalculatorModel.java

The Model performs all the calculations needed
and that is it. It doesn't know the View
exists

CalculatorView.java

This is the View
Its only job is to display what the user sees
It performs no calculations, but instead passes
information entered by the user to whomever needs
it.

CalculatorController.java

The Controller coordinates interactions
between the View and Model

