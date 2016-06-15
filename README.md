# csv-emitter-birt-plugin
Automatically exported from code.google.com/p/csv-emitter-birt-plugin

BIRT (Business Intelligence Reporting Tools) is an open source Eclipse-based set of reporting and data visualization tools and technologies used to build rich information applications, in particular, web applications based on Java and J2EE.

The CSV Report Emitter plugin for BIRT is an Eclipse based emitter plugin which outputs and displays your BIRT report in CSV Format.

The CSV Report Emitter plugin currently supports emitting a single table within a report design with Column Headers as First Row. This emitter handles Row/Cell level hidden properties while emitting the output.

##Update 06/14/2016
Add a new format "view.csv" in plugin.xml.  This is due to that Actuate iServer (tested in v11sp4fix3) would overwrite csv exporting with org.eclipse.birt.engine.dataextraction.csv when using JSAPI for download.  This results in CSV exporting dataset rather than (first) table, i.e. report content.  Notice that apart from deploying the JAR file to AcServer/MyClasses/eclipse/plugins, you also need to modifiy AcServer/etc/jfctsrvrconfig.xml and add "view.csv:com.actuate.birt.report.engine.emitter.csv2" in node "BIRTReportRenderingOption" -> entry "RenderFormatEmitterIdMapping".
