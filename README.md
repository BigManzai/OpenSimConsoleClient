# OpenSimConsoleClient
Eine Qt basierter Client für die OpenSimulator REST Konsole (Fernbedienung des OpenSimulators)

Dies ist die Deutsche Version

Das kompilieren ist etwas kniffelig deswegen ist in der ZIP Datei ConsoleClientGerman.zip alles fertig drin.

Ihr braucht das nur entpacken und starten.

Ihr müsst aber in jeder OpenSim.ini die Rest Konsole einschalten und den OpenSimulator folgendermaßen starten:

# Auszug OpenSim.ini
     [Network]
         ;# {ConsoleUser} {} {User name for console account} {}
         ;; Configure the remote console user here. This will not actually be used
         ;; unless you use -console=rest at startup.
         ConsoleUser = "Wunschname"
         ;# {ConsolePass} {} {Password for console account} {}
         ConsolePass = "Wunschpasswort"
         ;# {console_port} {} {Port for console connections} {} 0
         console_port = 0

         ;# {http_listener_port} {} {TCP Port for this simulator to listen on? (This must be unique to the simulator!)} {} 9000
         ;; Simulator HTTP port. This is not the region port, but the port the
         ;; entire simulator listens on. This port uses the TCP protocol, while
         ;; the region ports use UDP.
         http_listener_port = 9000

# Starteigenschaften
     OpenSim.exe -console rest
oder so
     mono OpenSim.exe -console rest
oder so
     screen -fa -S OS -d -U -m mono OpenSim.exe -console rest