# OpenEduAnalytics
OpenEduAnalytics is a fully open-sourced [(MIT license)](https://github.com/microsoft/OpenEduAnalytics/blob/main/LICENSE) data integration and analytics solution for the education sector.

You can setup a fully functional test environment with a test data set in 3 steps:
1) Open cloud shell in your azure subscription (use ctrl+click on the button below to open in a new page)\
[![Launch Cloud Shell](https://shell.azure.com/images/launchcloudshell.png "Launch Cloud Shell")](https://shell.azure.com/bash)
2) Download this repo to your azure clouddrive \
`cd clouddrive`\
`git clone https://github.com/microsoft/OpenEduAnalytics`
3) Run the setup script\
`./OpenEduAnalytics/setup_testenv.sh`

Because of issues with automating the provisioning of Synapse Notebooks, these additional steps are currently required for now...
4) In the cloud shell window, click on the upload/download icon, select "Manage file share", navigate to OpenEduAnalytics, download the notebook within each module and package folder.
5) In the cloud shell window, click on the link for your newly created Synapse instance
6) In Synapse, click on Develop, click on the "+", and select "Import", then multi-select all of the notebooks you just downloaded, and complete the import.
7) Open each notebook in Synapse, and do the following:
	* ensure that the "Attach to" dropdown is set to "spark1"
	* ensure that the "Language" dropdown is set to "PySpark"
	* click on "Run all" (make sure to run the Contoso_ISD notebook last because it depends on the others)

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.