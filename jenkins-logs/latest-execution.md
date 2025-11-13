# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_Polaris_Sarif_Report_Scan/main`
- **Build Number:** #3
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 4 min 2 sec and counting
- **Timestamp:** 2025-11-13 15:25:28 UTC

---

## Console Output

```
Started by user admin
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from e969c8d2c9ede42ea9998742f5871b49c9f308b2
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision e969196a63b1be83b84541b022f7aa52928bd5e5
The recommended git tool is: NONE
using credential Github_Username_PAT
 > git rev-parse --resolve-git-dir /Users/madhusud/.jenkins/workspace/b_Polaris_Sarif_Report_Scan_main@libs/a0dda568bac7bbb4a171f59ba3f2660c21c69edc6356524e9ae8bb4500c12bbb/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Fetching without tags
Fetching upstream changes from https://github.com/integrations-garage/blackduck-logs-publisher
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/integrations-garage/blackduck-logs-publisher +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision e969196a63b1be83b84541b022f7aa52928bd5e5 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
Commit message: "Phase 3 - 2"
 > git rev-list --no-walk e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
[Pipeline] Start of Pipeline
[Pipeline] node
Running on mac-sh in /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential Github_Username_PAT
Fetching changes from the remote Git repository
Fetching without tags
 > git rev-parse --resolve-git-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/.git # timeout=10
 > git config remote.origin.url https://github.com/polaris-jenkins-samples/sarif-report.git # timeout=10
Fetching upstream changes from https://github.com/polaris-jenkins-samples/sarif-report.git
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/polaris-jenkins-samples/sarif-report.git +refs/heads/main:refs/remotes/origin/main # timeout=10
Checking out Revision e969c8d2c9ede42ea9998742f5871b49c9f308b2 (main)
Commit message: "Delete jenkins-logs directory"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f e969c8d2c9ede42ea9998742f5871b49c9f308b2 # timeout=10
 > git rev-list --no-walk b2961442baf928a1b6b4b179b963800b88b23480 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] script
[Pipeline] {
[Pipeline] echo
JOB_NAME: MBP_Github_Polaris_Sarif_Report_Scan/main
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] sh
+ node --version
v22.16.0
[Pipeline] sh
+ npm --version
10.9.2
[Pipeline] sh
+ npm install
npm warn deprecated fsevents@1.2.9: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.

up to date, audited 1412 packages in 20s

32 packages are looking for funding
  run `npm fund` for details

136 vulnerabilities (9 low, 35 moderate, 57 high, 35 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (polaris-sarif-report)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] security_scan
**************************** START EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Sarif_Report_Scan
-------------------------------- Connection to node --------------------------------
[Security Scan] INFO: Jenkins job is running on agent node remotely
-------------------------- Parameter Validation Initiated --------------------------
[Security Scan] INFO:  --- product = [POLARIS]
[Security Scan] INFO: Parameters for polaris:
[Security Scan] INFO:  --- polaris_waitForScan = true
[Security Scan] INFO:  --- polaris_server_url = https://poc.polaris.blackduck.com
[Security Scan] INFO:  --- polaris_assessment_types = SAST,SCA
[Security Scan] INFO:  --- polaris_access_token = ******************************************************************************
[Security Scan] INFO:  --- polaris_reports_sarif_groupSCAIssues = true
[Security Scan] INFO:  --- polaris_reports_sarif_create = true
[Security Scan] INFO:  --- polaris_reports_sarif_severities = CRITICAL,HIGH
------------------------------------------------------------------------------------
[Security Scan] INFO: Parameters for additional configuration:
[Security Scan] INFO:  --- network_airgap = false
[Security Scan] INFO: Polaris parameters are validated successfully
[Security Scan] INFO: Bridge download parameters are validated successfully
[Security Scan] INFO: Bridge download is not required. Found installed in: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
------------------------------------------------------------------------------------
[Security Scan] INFO: Bridge CLI version is - 3.9.2
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Sarif_Report_Scan
[Security Scan] INFO: Polaris Application Name: sarif-report
[Security Scan] INFO: Polaris Project Name: sarif-report
[Security Scan] INFO: Polaris Branch Name: main
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Sarif_Report_Scan
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage polaris --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/polaris_input18003532925694439616.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-13 15:22:03.0897 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-13 15:22:03.1017 IST [Bridge CLI] INFO: Found version "3.0.371" in registry for workflow "polaris", trying to load it from local cache
2025-11-13 15:22:04.4090 IST [Bridge CLI] INFO: Input Resources:
2025-11-13 15:22:04.4090 IST [Bridge CLI] INFO: resource = value [source]
2025-11-13 15:22:04.4090 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 15:22:04.4090 IST [Bridge CLI] INFO: network.airgap = false [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.accesstoken = ***************************************** [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.application.name = sarif-report [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.assessment.types = [SAST SCA] [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.branch.name = main [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.project.name = sarif-report [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.reports.sarif.create = true [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.reports.sarif.file.path = .blackduck/integrations/polaris/sarif/report.sarif.json [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.reports.sarif.groupSCAIssues = true [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.reports.sarif.severities = [CRITICAL HIGH] [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.serverUrl = https://poc.polaris.blackduck.com [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: polaris.waitForScan = true [polaris_input18003532925694439616.json]
2025-11-13 15:22:04.4091 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 15:22:04.4092 IST [Bridge CLI] INFO: Starting adapters for stage polaris
2025-11-13 15:22:04.4107 IST [Bridge CLI] INFO: Starting Adapter: Polaris Status Provider
2025-11-13 15:22:04.4108 IST [Bridge CLI] INFO: Starting Adapter: Polaris Initializer
2025-11-13 15:22:04.4108 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCM Discovery
2025-11-13 15:22:04.4108 IST [Bridge CLI] INFO: Starting Adapter: Polaris Controller
2025-11-13 15:22:04.4842 IST [Polaris SCM Discovery] INFO: Adapter finished
2025-11-13 15:22:04.4877 IST [Bridge CLI] INFO: Starting Adapter: Set Polaris Assessment Mode to CI
2025-11-13 15:22:04.4881 IST [Set Polaris Assessment Mode to CI] INFO: Provided value for resource 'polaris.assessment.mode'
2025-11-13 15:22:04.4883 IST [Set Polaris Assessment Mode to CI] INFO: Adapter finished
2025-11-13 15:22:04.4916 IST [Bridge CLI] INFO: Starting Adapter: Create Polaris Project & Branch By Default
2025-11-13 15:22:04.4917 IST [Create Polaris Project & Branch By Default] INFO: Provided value for resource 'polaris.onboarding'
2025-11-13 15:22:04.4917 IST [Create Polaris Project & Branch By Default] INFO: Adapter finished
2025-11-13 15:22:07.4009 IST [Polaris Initializer] INFO: Successfully created test for "SCA(scaPackage)" assessment. The short test ID is "E6U3PDJ"
2025-11-13 15:22:11.1710 IST [Polaris Initializer] INFO: Successfully created test for "SAST(sastFull)" assessment. The short test ID is "TUWPI2T"
2025-11-13 15:22:11.2005 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.id'
2025-11-13 15:22:11.2009 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.id'
2025-11-13 15:22:11.2012 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.shortId'
2025-11-13 15:22:11.2015 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.shortId'
2025-11-13 15:22:11.2021 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.streamId'
2025-11-13 15:22:11.2027 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.project.id'
2025-11-13 15:22:11.2029 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.branch.id'
2025-11-13 15:22:11.2032 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.portfolioid'
2025-11-13 15:22:11.2034 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.tenant.id'
2025-11-13 15:22:11.2036 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.application.id'
2025-11-13 15:22:11.2040 IST [Polaris Initializer] INFO: Adapter finished
2025-11-13 15:22:11.2269 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-13 15:22:11.2737 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-13 15:22:11.2740 IST [Check pull request] INFO: Adapter finished
2025-11-13 15:22:11.3147 IST [Polaris Controller] INFO: Running for "sast" assessment with scan type "sastFull"
2025-11-13 15:22:11.3150 IST [Polaris Controller] INFO: fetching recommended "coverity" tool info...
2025-11-13 15:22:16.1870 IST [Polaris Controller] INFO: checking "coverity" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0
2025-11-13 15:22:16.1871 IST [Polaris Controller] INFO: Checking tool version for "cov_thin_client" in "/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0"
2025-11-13 15:22:16.1878 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity --version
2025-11-13 15:22:16.2755 IST [Polaris Controller] INFO: Got tool version for "cov_thin_client": 2025.9.0
2025-11-13 15:22:17.2007 IST [Polaris Controller] INFO: "coverity" tool is already installed...
2025-11-13 15:22:17.2008 IST [Polaris Controller] INFO: fetching recommended "Sigma" tool info...
2025-11-13 15:22:18.4757 IST [Polaris Controller] INFO: checking "Sigma" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0
2025-11-13 15:22:18.4758 IST [Polaris Controller] INFO: Checking tool version for "sigma" in "/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0"
2025-11-13 15:22:18.4761 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --version
2025-11-13 15:22:18.5992 IST [Polaris Controller] INFO: Got tool version for "sigma": 2025.10.0
2025-11-13 15:22:19.5419 IST [Polaris Controller] INFO: "Sigma" tool is already installed...
2025-11-13 15:22:19.5420 IST [Polaris Controller] INFO: Running for "sca" assessment with scan type "scaPackage"
2025-11-13 15:22:19.5420 IST [Polaris Controller] INFO: fetching recommended "detect" tool info...
2025-11-13 15:22:19.8582 IST [Polaris Controller] INFO: checking "detect" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0
2025-11-13 15:22:19.8583 IST [Polaris Controller] INFO: Running command:/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -version
2025-11-13 15:22:20.2516 IST [Polaris Controller] INFO: Checking tool version for "detect" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0"
2025-11-13 15:22:20.2557 IST [Polaris Controller] INFO: Got tool version for "detect": 10.4.0
2025-11-13 15:22:20.5467 IST [Polaris Controller] INFO: "detect" tool is already installed...
2025-11-13 15:22:20.5815 IST [Polaris Controller] INFO: Provided value for resource 'coverity.id'
2025-11-13 15:22:20.5817 IST [Polaris Controller] INFO: Provided value for resource 'sigma.id'
2025-11-13 15:22:20.5818 IST [Polaris Controller] INFO: Provided value for resource 'detect.id'
2025-11-13 15:22:20.5819 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sast
2025-11-13 15:22:20.5819 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sca-package
2025-11-13 15:22:20.5819 IST [Bridge CLI] INFO: Starting adapters for stage polaris-artifacts-uploader
2025-11-13 15:22:20.5819 IST [Bridge CLI] INFO: Starting adapters for stage polaris-post-processing
2025-11-13 15:22:20.5819 IST [Bridge CLI] INFO: Starting adapters for stage polaris-reports-sarif
2025-11-13 15:22:20.5836 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCA Package Manager Scan
2025-11-13 15:22:20.5836 IST [Bridge CLI] INFO: Starting Adapter: Polaris Coverity Capture
2025-11-13 15:22:20.5837 IST [Bridge CLI] INFO: Starting Adapter: Polaris Artifacts Uploader
2025-11-13 15:22:20.5842 IST [Polaris Controller] INFO: Adapter finished
2025-11-13 15:22:20.5837 IST [Bridge CLI] INFO: Starting Adapter: Polaris Waiter
2025-11-13 15:22:20.5837 IST [Bridge CLI] INFO: Starting Adapter: Polaris Issues Fetcher
2025-11-13 15:22:20.5837 IST [Bridge CLI] INFO: Starting Adapter: Polaris Policy Checker
2025-11-13 15:22:20.5838 IST [Bridge CLI] INFO: Starting Adapter: Polaris SARIF Issues Fetcher
2025-11-13 15:22:20.6261 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 15:22:20.6265 IST [Default Adapter for execution path] INFO: Provided value for resource 'coverity.execution.path'
2025-11-13 15:22:20.6266 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 15:22:20.6374 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 15:22:20.6375 IST [Default Adapter for execution path] INFO: Provided value for resource 'sigma.execution.path'
2025-11-13 15:22:20.6376 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 15:22:20.7198 IST [Polaris Coverity Capture] INFO: Identified workflow: Polaris
2025-11-13 15:22:20.7211 IST [Polaris Coverity Capture] INFO: command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity capture --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -o analyze.location=connect
2025-11-13 15:22:20.7796 IST [Polaris Coverity Capture] INFO: coverity 2025.9.0 covcli-2025.9-push-12
2025-11-13 15:22:20.7798 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_API_TOKEN_FILE=/var/folders/wm/gkd75sk54h57yqd0_j95gp2r0000gn/T/polaris_coverity_cache1188276038/.authKey
2025-11-13 15:22:20.7798 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_KEY=187668b0-e8f2-41c9-927d-a6565857dcf7
2025-11-13 15:22:20.7798 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_URL=https://poc.polaris.blackduck.com/api/cache
2025-11-13 15:22:20.7798 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CLI_CAPTURE_ZIP_ARCHIVE=/Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip
2025-11-13 15:22:20.7798 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CLI_POLARIS_CLIENT=true
2025-11-13 15:22:20.7847 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir reset-host-name
2025-11-13 15:22:20.8325 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir check-compatible
2025-11-13 15:22:20.8608 IST [Polaris Coverity Capture] INFO: Detected that stdout is not connected to a terminal.  Defaulting ticker mode to 'none'.
2025-11-13 15:22:20.8608 IST [Polaris Coverity Capture] INFO: If this is not correct, explicitly set the ticker mode to the desired value using the '--ticker-mode' option.
2025-11-13 15:22:20.8633 IST [Polaris Coverity Capture] INFO: Using lightweight capture with thin client.
2025-11-13 15:22:20.8635 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-internal-manage-cache check
2025-11-13 15:22:21.7193 IST [Polaris Coverity Capture] INFO: Caching is enabled.
2025-11-13 15:22:21.7232 IST [Polaris Coverity Capture] INFO: Telemetry is enabled
2025-11-13 15:22:22.6795 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:22:22.7048 IST [Polaris Coverity Capture] INFO: Executing action no-op: nothing to do for initialization
2025-11-13 15:22:23.1974 IST [Polaris Coverity Capture] INFO: Executing action no-op: skipping compiler configuration
2025-11-13 15:22:23.6357 IST [Polaris Coverity Capture] INFO: Executing action no-op: no compilers need to be unconfigured
2025-11-13 15:22:24.0508 IST [Polaris Coverity Capture] INFO: Executing action no-op: compiler configurations loaded
2025-11-13 15:22:24.6039 IST [Polaris Coverity Capture] INFO: Executing action Emit files using buildless capture: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-internal-capture-files --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --ticker-mode none --append-log --capture-list-file /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/capture-file-list-3946114398 --record-with-source
2025-11-13 15:22:24.6436 IST [Polaris Coverity Capture] INFO: Buildless capture started.
2025-11-13 15:22:24.6604 IST [Polaris Coverity Capture] INFO: Emitting 84 Files.
2025-11-13 15:22:24.8682 IST [Polaris Coverity Capture] INFO: Buildless capture completed.
2025-11-13 15:22:24.8703 IST [Polaris Coverity Capture] INFO: Executing action No unwanted TUs to delete
2025-11-13 15:22:24.8703 IST [Polaris Coverity Capture] INFO: Executing action Action cleanup: Unwanted TUs action cleanup
2025-11-13 15:22:24.8704 IST [Polaris Coverity Capture] INFO: Executing action deleteResidualTUs /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir
2025-11-13 15:22:24.8706 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:22:24.8869 IST [Polaris Coverity Capture] INFO: Executing action Invalidate capture results
2025-11-13 15:22:24.8869 IST [Polaris Coverity Capture] INFO: Executing action Invoke cov-run-sigma: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-run-sigma --project-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir --coverity-config /var/folders/wm/gkd75sk54h57yqd0_j95gp2r0000gn/T/cov-run-sigma-config-3876918417/coverity.yaml --sigma-binary-path /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --enable-telemetry
2025-11-13 15:22:24.9184 IST [Polaris Coverity Capture] INFO: cov-run-sigma version 2025.9.0 on Darwin 24.6.0 arm64
2025-11-13 15:22:24.9184 IST [Polaris Coverity Capture] INFO: Internal version numbers: 477d3c5ddd p-2025.9-push-57
2025-11-13 15:22:24.9185 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:22:26.5551 IST [Polaris Coverity Capture] INFO: Executing action Action cleanup: Coverity configuration for Sigma
2025-11-13 15:22:27.0594 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:22:27.1255 IST [Polaris Coverity Capture] INFO: Capture summary:
2025-11-13 15:22:27.1255 IST [Polaris Coverity Capture] INFO:     SUCCEEDED: 88
2025-11-13 15:22:27.1255 IST [Polaris Coverity Capture] INFO:     INCOMPLETE: 0
2025-11-13 15:22:27.1255 IST [Polaris Coverity Capture] INFO:     FAILED: 0
2025-11-13 15:22:27.1255 IST [Polaris Coverity Capture] INFO:     IGNORED: 3
2025-11-13 15:22:27.1255 IST [Polaris Coverity Capture] INFO:     FILES CAPTURED: 88
2025-11-13 15:22:27.1256 IST [Polaris Coverity Capture] INFO:     LINES OF CODE: 32922
2025-11-13 15:22:27.1278 IST [Polaris Coverity Capture] INFO: Capture phase took 5.411s.
2025-11-13 15:22:27.1278 IST [Polaris Coverity Capture] WARNING: !! SOURCES FOR UNSUPPORTED LANGUAGES WERE DETECTED !!
2025-11-13 15:22:27.1278 IST [Polaris Coverity Capture] WARNING: 
2025-11-13 15:22:27.1278 IST [Polaris Coverity Capture] WARNING: Source files for the following languages were detected, but these languages are not supported on Mac OS ARM:
2025-11-13 15:22:27.1278 IST [Polaris Coverity Capture] WARNING:   * C#
2025-11-13 15:22:27.1278 IST [Polaris Coverity Capture] WARNING: In order to analyze these files, please analyze the project on an operating system and architecture where they are supported.
2025-11-13 15:22:27.1539 IST [Polaris Coverity Capture] INFO: To analyze your project, type '/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity analyze --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -o analyze.location=connect'.
2025-11-13 15:22:27.1555 IST [Polaris Coverity Capture] INFO: Coverity Capture completed successfully
2025-11-13 15:22:27.1622 IST [Polaris Coverity Capture] INFO: Provided value for resource 'coverity.completed'
2025-11-13 15:22:27.1624 IST [Polaris Coverity Capture] INFO: Provided value for resource 'coverity.idir.output'
2025-11-13 15:22:27.1625 IST [Polaris Coverity Capture] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.artifacts.path'
2025-11-13 15:22:27.1627 IST [Polaris Coverity Capture] INFO: Adapter finished
2025-11-13 15:22:27.1649 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 15:22:27.1650 IST [Default Adapter for execution path] INFO: Provided value for resource 'detect.execution.path'
2025-11-13 15:22:27.1651 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 15:22:27.2127 IST [Polaris SCA Package Manager Scan] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0/detect-10.4.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect --detect.tools=DETECTOR --detect.component.location.analysis.enabled=true --blackduck.offline.mode=true --blackduck.offline.mode.force.bdio=true
2025-11-13 15:22:27.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Self-Update feature is disabled because of the following reasons:
2025-11-13 15:22:27.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Detect in offline mode is incompatible with the Self-Update feature.
2025-11-13 15:22:27.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Black Duck URL is required for the Self-Update feature.
2025-11-13 15:22:28.2692 IST [Polaris SCA Package Manager Scan] INFO: ______     _            _
2025-11-13 15:22:28.2693 IST [Polaris SCA Package Manager Scan] INFO: |  _  \   | |          | |
2025-11-13 15:22:28.2693 IST [Polaris SCA Package Manager Scan] INFO: | | | |___| |_ ___  ___| |_
2025-11-13 15:22:28.2693 IST [Polaris SCA Package Manager Scan] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-13 15:22:28.2693 IST [Polaris SCA Package Manager Scan] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-13 15:22:28.2693 IST [Polaris SCA Package Manager Scan] INFO: |___/ \___|\__\___|\___|\__|
2025-11-13 15:22:28.2694 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 15:22:28.4011 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 15:22:28.4011 IST [Polaris SCA Package Manager Scan] INFO: Detect Version: 10.4.0
2025-11-13 15:22:28.4012 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Current property values:
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- --property = value [notes]
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode = true [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode.force.bdio = true [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.component.location.analysis.enabled = true [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge [env] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.tools = DETECTOR [cmd] 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect build date: 2025-04-24
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-09-52-28-357
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Correlated Scanning is not available for Rapid/Stateless scan mode or offline scanning. A correlation ID will not be set.
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Docker tool will not be run.
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Bazel tool will not be run.
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Will include the Detectors tool.
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Searching for detectors.
2025-11-13 15:22:28.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detector Report
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm (depth 0)
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/package-lock.json
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/package.json
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detectors actions finished.
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project name: owasp-nodejs-goat
2025-11-13 15:22:29.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project version: 1.3.0
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Signature Scanner tool will not be run.
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- IaC Scanner tool will not be run.
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  Product Notice                                                                                #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  © 2024 Black Duck Software, Inc.                                                              #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  This Black Duck Component Locator and all associated documentation are proprietary            #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  to Black Duck Software, Inc. and may only be used pursuant to the terms and conditions of a   #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  written license agreement with Black Duck Software, Inc. All other use, reproduction,         #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  modification, or distribution of the Black Duck Component Locator or the associated           #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  documentation is strictly prohibited.                                                         #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 15:22:30.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Running Component Locator v1.1.12 on /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis file saved at: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-09-52-28-357/scan/components-with-locations.json
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-09-52-28-357/status/status.json
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Result ========
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis File: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-09-52-28-357/scan/components-with-locations.json
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Status ========
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- NPM: SUCCESS
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ===============================
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:23:13.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect duration: 00h 00m 45s 644ms
2025-11-13 15:23:13.1998 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'detect.completed'
2025-11-13 15:23:13.2000 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.path'
2025-11-13 15:23:13.2002 IST [Polaris SCA Package Manager Scan] INFO: Adapter finished
2025-11-13 15:23:13.2593 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SCA(scaPackage)" assessment with id "658ec189-5ecb-4ea7-a0c9-551091abab95"
2025-11-13 15:23:13.2598 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SAST(sastFull)" assessment with id "86f391fb-3f9d-4511-926b-d023cfd0720c"
2025-11-13 15:23:14.6116 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip for "SCA(scaPackage)" assessment
2025-11-13 15:23:15.2860 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:   7%  16384/208944
2025-11-13 15:23:15.4933 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  39%  81920/208944
2025-11-13 15:23:15.4951 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  70%  147456/208944
2025-11-13 15:23:15.9163 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact: 100%  208944/208944
2025-11-13 15:23:16.3772 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip"
2025-11-13 15:23:16.9057 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SCA(scaPackage)" assessment with id "658ec189-5ecb-4ea7-a0c9-551091abab95"
2025-11-13 15:23:18.4153 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip for "SAST(sastFull)" assessment
2025-11-13 15:23:18.8591 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:   3%  16384/417838
2025-11-13 15:23:19.0682 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  31%  131072/417838
2025-11-13 15:23:19.4879 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  58%  245760/417838
2025-11-13 15:23:19.6983 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  86%  360448/417838
2025-11-13 15:23:19.6994 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact: 100%  417838/417838
2025-11-13 15:23:20.1698 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip"
2025-11-13 15:23:20.6289 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SAST(sastFull)" assessment with id "86f391fb-3f9d-4511-926b-d023cfd0720c"
2025-11-13 15:23:20.6527 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.artifacts.uploadSuccessful'
2025-11-13 15:23:20.6530 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.uploadSuccessful'
2025-11-13 15:23:20.6535 IST [Polaris Artifacts Uploader] INFO: Adapter finished
2025-11-13 15:23:20.7115 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SAST(sastFull)" and id "86f391fb-3f9d-4511-926b-d023cfd0720c"
2025-11-13 15:23:20.7120 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SCA(scaPackage)" and id "658ec189-5ecb-4ea7-a0c9-551091abab95"
2025-11-13 15:23:21.4964 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "658ec189-5ecb-4ea7-a0c9-551091abab95" is "Queuing"
2025-11-13 15:23:21.5115 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "86f391fb-3f9d-4511-926b-d023cfd0720c" is "Queuing"
2025-11-13 15:24:02.7105 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "658ec189-5ecb-4ea7-a0c9-551091abab95" is "Scanning & Publishing"
2025-11-13 15:24:02.7224 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "86f391fb-3f9d-4511-926b-d023cfd0720c" is "Scanning"
2025-11-13 15:24:13.0150 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "658ec189-5ecb-4ea7-a0c9-551091abab95" is "In Progress"
2025-11-13 15:24:13.0199 IST [Polaris Waiter] INFO: test with assessment type "SAST(sastFull)" and id "86f391fb-3f9d-4511-926b-d023cfd0720c" completed successfully
2025-11-13 15:24:23.3305 IST [Polaris Waiter] INFO: test with assessment type "SCA(scaPackage)" and id "658ec189-5ecb-4ea7-a0c9-551091abab95" completed successfully
2025-11-13 15:24:23.3657 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.completed'
2025-11-13 15:24:23.3662 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.completed'
2025-11-13 15:24:23.3670 IST [Polaris Waiter] INFO: Adapter finished
2025-11-13 15:24:23.4638 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SAST(sastFull)" assessment...
2025-11-13 15:24:23.4644 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SCA(scaPackage)" assessment...
2025-11-13 15:24:24.3611 IST [Polaris Policy Checker] INFO: no policies were violated to break the build
2025-11-13 15:24:24.3908 IST [Polaris Policy Checker] INFO: Adapter finished
2025-11-13 15:24:24.4429 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SAST(sastFull)" assessment
2025-11-13 15:24:24.4435 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SCA(scaPackage)" assessment
2025-11-13 15:24:25.2606 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SAST(sastFull)" with id "86f391fb-3f9d-4511-926b-d023cfd0720c"
 {
 "critical": 0,
 "high": 2,
 "informational": 0,
 "low": 25,
 "medium": 13
}
2025-11-13 15:24:25.3383 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SCA(scaPackage)" with id "658ec189-5ecb-4ea7-a0c9-551091abab95"
 {
 "critical": 6,
 "high": 109,
 "informational": 0,
 "low": 15,
 "medium": 133
}
2025-11-13 15:24:25.3797 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.critical'
2025-11-13 15:24:25.3802 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.informational'
2025-11-13 15:24:25.3806 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.low'
2025-11-13 15:24:25.3811 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.high'
2025-11-13 15:24:25.3816 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.medium'
2025-11-13 15:24:25.3821 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.critical'
2025-11-13 15:24:25.3825 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.informational'
2025-11-13 15:24:25.3829 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.high'
2025-11-13 15:24:25.3834 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.low'
2025-11-13 15:24:25.3838 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.medium'
2025-11-13 15:24:25.3847 IST [Polaris Issues Fetcher] INFO: Adapter finished
2025-11-13 15:24:25.8691 IST [Polaris SARIF Issues Fetcher] INFO: Fetching issues from Polaris Server...
2025-11-13 15:25:27.0920 IST [Polaris SARIF Issues Fetcher] INFO: Added entry to resource 'polaris.reports.sarif.issues'
2025-11-13 15:25:27.0989 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sarif-generator
2025-11-13 15:25:27.0990 IST [Bridge CLI] INFO: Starting Adapter: Polaris SARIF Generator
2025-11-13 15:25:27.0993 IST [Polaris SARIF Issues Fetcher] INFO: Adapter finished
2025-11-13 15:25:27.1532 IST [Polaris Status Provider] INFO: Results for test "SAST(sastFull)" with ID "86f391fb-3f9d-4511-926b-d023cfd0720c" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/3155375b-3f50-48e7-9737-7584ba73951e/projects/251f9942-e5a9-459b-bcf7-84f4dc25d7d7/tests/86f391fb-3f9d-4511-926b-d023cfd0720c/detected-issues
2025-11-13 15:25:27.1535 IST [Polaris Status Provider] INFO: Results for test "SCA(scaPackage)" with ID "658ec189-5ecb-4ea7-a0c9-551091abab95" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/3155375b-3f50-48e7-9737-7584ba73951e/projects/251f9942-e5a9-459b-bcf7-84f4dc25d7d7/tests/658ec189-5ecb-4ea7-a0c9-551091abab95/detected-issues
2025-11-13 15:25:27.1535 IST [Polaris Status Provider] INFO: Polaris issues view for project "sarif-report", branch "main" is available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/3155375b-3f50-48e7-9737-7584ba73951e/projects/251f9942-e5a9-459b-bcf7-84f4dc25d7d7/issues?branchId=3d1f3651-8c0b-4b62-a7a7-19573df6e09c
2025-11-13 15:25:27.1607 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.summary.url'
2025-11-13 15:25:27.1609 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.summary.url'
2025-11-13 15:25:27.1610 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.project.issues.url'
2025-11-13 15:25:27.1612 IST [Polaris Status Provider] INFO: Adapter finished
2025-11-13 15:25:27.6433 IST [Polaris SARIF Generator] INFO: Will create rules with SCA component-version pairs grouped by their related vulnerabilities in the SARIF report. Since "polaris.reports.sarif.groupSCAIssues" is configured to "true"
2025-11-13 15:25:27.6499 IST [Polaris SARIF Generator] INFO: SARIF report created successfully at .blackduck/integrations/polaris/sarif/report.sarif.json
2025-11-13 15:25:27.6679 IST [Polaris SARIF Generator] INFO: Provided value for resource 'polaris.reports.sarif.file.output'
2025-11-13 15:25:27.6687 IST [Polaris SARIF Generator] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: This is not a (PR/MR) event
[Security Scan] INFO: Archiving SARIF jenkins artifact from: /Users/madhusud/Jenkins_Testing/Nodes/workspace/b_Polaris_Sarif_Report_Scan_main/nodejs-npm/.blackduck/integrations/polaris/sarif/report.sarif.json
Archiving artifacts
[Security Scan] INFO: SARIF archived successfully in jenkins artifact
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Total issues found: 303
[Security Scan] INFO: Security Scan execution is successful
**************************** END EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Black Duck Logs Publisher - Starting log upload process
[Pipeline] echo
Configuration: [githubOrg:polaris-jenkins-samples, repoName:sarif-report, credentialsId:github-pat-logs-publisher, maxRetries:3, retentionCount:5, jobNamePrefixes:[MBP_Github_, MBP_, Github_, Pipeline_, Job_, Build_]]
[Pipeline] echo
Job Name: MBP_Github_Polaris_Sarif_Report_Scan/main
[Pipeline] echo
Build Number: 3
[Pipeline] echo
GitHub Organization: polaris-jenkins-samples
[Pipeline] withCredentials
Masking supported pattern matches of $GITHUB_TOKEN
[Pipeline] {
[Pipeline] echo
Using configured repository name: sarif-report
[Pipeline] echo
Target repository: polaris-jenkins-samples/sarif-report
[Pipeline] echo
LogProcessor: captureJenkinsLogs called
```

---

*Log generated by Black Duck Logs Publisher*