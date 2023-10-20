https://www.tp-link.com/no/support/download/oc300/v1/?app=web#Omada_Discovery_Utility
使用Hxd工具未搜索到log4j

omada discovery实用程序分析：
	Omada_Discovery_Utility_5.0.8.zip：log4j-core-2.16.0.jar由omada-discovery-utility-5.0.8.jar（Hxd可以查到）引入，无log4j漏洞
	Omada_Discovery_Utility_4.2.4.zip：omada-discovery-utility-4.2.4.jar（Hxd可以查到）解包后出现org/apache/logging/log4j/core/lookup/JndiLookup.class（MD5：641fd7ae76e95b35f02c55ffbf430e6b），存在log4j漏洞
	omada-discovery-utility-3.2.1.zip：omada-discovery-utility-3.2.1.jar（Hxd可以查到）解包后出现org/apache/logging/log4j/core/lookup/JndiLookup.class（MD5：641fd7ae76e95b35f02c55ffbf430e6b），存在log4j漏洞
	
固件分析：
	OC300_UN_v1_1.1.0_Build_20210406.zip：OC300v1_un_1.1.0_20210406_rel58776_up.bin（Hxd可以查到）解包后存在log4j-core-2.8.2.jar，因为正好处于8层，存在log4j漏洞
	OC300_UN_v1_1.19.3_20230906.zip：OC300v1_un_1.19.3_20230906_rel38429_up.bin（Hxd可以查到）解包后存在log4j-core-2.17.1.jar,大于2.15版本，无log4j漏洞