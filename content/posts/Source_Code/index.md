+++
title = 'Source code'
summary = "View our code in detail"
draft = false
weight = 10
+++

The source code for this web report is available [here](https://github.com/andergisomon/efb2073_report "Title"). Source code for the ESP32C3 boards are available [here](https://github.com/andergisomon/esp-idf-learning/ "Title").

### Transmitter program
{{< highlight C "linenos=table" >}}
{{< fetchfile url="https://raw.githubusercontent.com/andergisomon/esp-idf-learning/main/transmitter.c" >}}
{{< /highlight >}}

### Receiver program
{{< highlight C "linenos=table" >}}
{{< fetchfile url="https://raw.githubusercontent.com/andergisomon/esp-idf-learning/main/receiver.c" >}}
{{< /highlight >}}

### Data logging
The logging functionality requires a Powershell instance using the IDF frontend:
{{< highlight Bash "linenos=table" >}}
PS cd /path/to/idf/project
PS idf.py -p COMX monitor > logfile.txt
{{< /highlight >}}

The log contents can be viewed as such:
{{< highlight Bash "linenos=table" >}}
PS Get-Content .\logfile.txt
{{< /highlight >}}