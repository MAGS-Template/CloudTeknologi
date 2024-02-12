# Netværksautomatisering med Python Kodeeksempler
Fra [Cisco-DevNet](https://github.com/CiscoDevNet)

En samling af Python Kodeeksempler til Netværksstyring. Indeholder eksempler, der udnytter on-box biblioteker, såvel som eksempler, der bruger eksterne API'er (NETCONF/RESTCONF, SNMP, SSH, REST osv.). Nogle eksempler bruger tilgængelige SDK'er. Vi kommer ikke til at gå igennem alle eksempler, da vi hurtigt går videre til Ansible og Terraform. Dog er det meget det samme koncepter som bliver brugt! 

## On-Box Eksempler

Mange Cisco-switches og routere har en on-box Python Interpreter, der kan udnyttes til at køre scripts og programmer direkte på slutenhederne. Ud over Interpreteren inkluderes Python-biblioteker, der giver direkte adgang til enhedens underliggende drift for at udføre CLI-kommandoer eller overvåge events.

### Kodeeksempler

|  Kodeeksempel  |  Beskrivelse  |
|  --- |  ---  |
|  [Udfør CLI via Python](/PythonEksempler/Py-sho-ver-onbox)  |  Dette eksempel er så simpelt som det bliver. Ved at udnytte CLI-biblioteket udfører vi kommandoen "show version" på enheden. |
|  [TDR Test på Alle Interface](/PythonEksempler/tdr-test)  |  Dette eksempel udnytter igen CLI-biblioteket, men for at gøre noget lidt mere interessant. Der udføres en TDR-test på alle grænseflader i "op" status.  |
|  [EEM Konfigurationsændringer til Spark](/PythonEksempler/eem_configdiff_to_spark)  |  I dette eksempel bruges EEM-biblioteket til at overvåge konfigurationsændringer. Når en ændring opstår, sendes en besked til et Cisco Spark-rum.  |
|  [Python med Eventing Eksempel](/PythonEksempler/EEM-interface-move-routes)  |  Brug EEM og Python sammen til at scripte baseret på lokale begivenheder. |
|  [EEM + Python + Spark ChatOps](/PythonEksempler/spark_checkin)  |  Brug EEM til at overvåge konfigurationsændringer og send en Spark-besked |  
|  [EEM + Python + E-mail alarm](/PythonEksempler/PortFlap_email_alert)  |  Dette eksempel udnytter CLI-biblioteket og bruger EEM-funktionen til at overvåge grænseflade-flappende og sende en e-mailalarm |

## Off-Box Eksempler

Her er nogle Python-scripts, der kan interagere med netværkselementer ved hjælp af en af de mange eksponerede interfaces (NETCONF, RESTCONF, SNMP, SSH osv.). Mange af disse scripts kan også køres on-box, men de udnytter ikke nogen af de unikke biblioteker, der er tilgængelige på enheden.

|  Kodeeksempel  |  Beskrivelse  |
|  --- |  ---  |
|  [Netmiko og CLI Eksempel til Interface-styring](/PythonEksempler/netmiko-interface-example)  |  Disse er en række python-scripts til at hente, oprette, slette en Loopback-Interface med Python.  | 
|  [MIB Walk med Python](/PythonEksempler/snmp_entity)  |  I dette eksempel udfører vi en MIB-walk mod en enhed ved hjælp af "netsnmp"-biblioteket til Python.  |
|  [NETCONF Forbindelse med Python](/PythonEksempler/netconf_entity)  |  Dette eksempel viser det grundlæggende i at forbinde til en enhed med NETCONF ved hjælp af "ncclient"-biblioteket til Python.  |
|  [Konfigurer Interface IP-adresse med RESTCONF](/PythonEksempler/restconf_update_ipaddress)  |  I dette eksempel bruges den nyere vedtagne RESTCONF-standard til at konfigurere IP-adressen på en grænseflade.  |
|  [Hent Inventar fra APIC-EM](/PythonEksempler/apic-em_get_inventory_stats)  |  APIC-EM vedligeholder en inventardatabase over hele netværket. I dette eksempel bruges Python til at hente den information ved hjælp af REST API'en.  |  
|  [Hent hostliste fra APIC-EM](/PythonEksempler/apic-em_get_hosts)  |  APIC-EM vedligeholder en liste over alle klienter, der er tilsluttet de netværksenheder, der er opdaget af APIC-EM. Dette eksempel forespørger APIC-EM for listen og viser den i en simpel tabel.  |
|  [Hent Tenants  fra ACI APIC](/PythonEksempler/acitoolkit_show_tenants)  |  Dette eksempel udnytter ACI Toolkit til at oprette forbindelse til en APIC-controller og hente listen over konfigurerede Tenants.  |  
|  [Grundlæggende NETCONF Hent](/PythonEksempler/NC-get-config)  |  Et grundlæggende ncclient-eksempel til `<get>` NETCONF Data  |
|  [Grundlæggende NETCONF Rediger](/PythonEksempler/NC-edit-config)  |  Et grundlæggende ncclient-eksempel til `<edit-config>` NETCONF Data  |  
|  [NETCONF XPATH Eksempel](/PythonEksempler/NC-get-config-xpath)  |  Brug XPATH-funktionen ved at foretage NETCONF-anmodninger  |  
|  [Model Baseret AAA](/PythonEksempler/model-based-aaa)  |  Disse eksempelskripter er til Model Baseret AAA for at få, redigere og slette regellisterne for privilegieniveau-brugere og grupper ved at bruge ietf-netconf-acm.yang datamodel  |
|  [RESTCONF](/PythonEksempler/RESTCONF)  |  Disse eksempelskripter er til RESTCONF til at h
