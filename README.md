# CME Smart Stream on GCP Python Tutorial Notebooks

This project contains a variety of python notebooks to support customers initial usage of [CME Smart Stream on Google Cloud Platform (GCP)](https://www.cmegroup.com/market-data/cloud-mdp.html).  Since Smart Stream on GCP leverages [Google Cloud Pub/Sub](https://cloud.google.com/pubsub/) as well as [Google IAM](https://cloud.google.com/iam/), the following notebook leverages [GCP Python](https://cloud.google.com/python/) libraries thereby removing the complexity of accessing CME Group Market Data while demonstrating the basic workflows needed to use the Cloud PubSub solution. 


# High Level View of Solution

CME Smart Stream on GCP leverages Google Cloud Pub/Sub to enable customers to access CME Group market data.  As the diagram illustrates below, CME Group pushes data into Topics and customers retrieve data from Subscriptions.  

![CME Smart Stream Overview Diagram](https://github.com/CMEGroup/CMESmartStream-on-GCP-Tutorial/blob/master/Tutorials/images/CloudPubSubOverview.png)


# Tutorial Overviews

## Getting CME Binary Data from Smart Stream on Google Cloud Platform

CME Smart Stream is designed to provide all CME Group market data via Cloud Pub/Sub Topics where customers can create Cloud Pub/Sub Subscriptions in their specific GCP projects.  In this [tutorial](https://github.com/CMEGroup/CMESmartStream-on-GCP-Tutorial/blob/master/Tutorials/GooglePubSubGetCMEBinaryData.ipynb):
- Credential via GCP IAM using your Service Account or User Account.
- Setup your Project and target a CME Group market data Topic.
- Create a Cloud Pub/Sub Subscription in your account.
- Pull a single message from that Queue.
- Delete the Subscription

## Downloading List of CME Group Market Data Topics Available on CME Smart Stream

CME Smart Stream on GCP has over 152 Market Data Topics available as aligned to CME [traditional on-premises multi-cast solutions](https://www.cmegroup.com/market-data/distributor/market-data-platform.html). 

This [tutorials](https://github.com/CMEGroup/CMESmartStream-on-GCP-Tutorial/blob/master/Tutorials/GooglePubSubGetCMEBinaryTopics.ipynb) shows how you can quickly download active list of Topics for Certification, New Release and Production.  


# Getting Started

## Sign up for CME Smart Stream on Google Cloud Platform

Please go to [CME Group Data Services Portal](http://dataservices.cmegroup.com/Data-Products) to register for CME Smart Stream on GCP.  Once approved, these examples will run with your specific GCP IAM information supplied at onboarding.


## To Run This Analysis Locally

To use the examples in Juptyer notebook from Anaconda Python.  The following will clone this repo, including an environment.yml file that will create the proper Anaconda environment with all the dependencies.  You then launch the Juptyer lab environment.  

```
git clone https://github.com/CMEGroup/CMESmartStream-on-GCP-Tutorial.git
cd CMESmartStream-on-GCP-Tutorial
conda env create .
source activate  CMESmartStream_on_GCP_Tutorial
jupyter notebook


```
Alternatively, you can use your own python environment but review the environment.yml file to determine the package dependencies.  The minimum dependencies are the [Google SDK](https://cloud.google.com/sdk/docs/quickstarts) and [Google Python Library](https://cloud.google.com/pubsub/docs/reference/libraries).


# Other Support for CME Smart Stream
Please use the Issues feature above to request new tutorials or adjustments as needed.  If you would like more information, please contact markettechsales@cmegroup.cmegroup for information.  


Those using Java can leverage our initial package for accessing a subscription and performing order sequencing.  

[CME Smart Stream Binary Data Sequencer](https://github.com/CMEGroup/CMESmartStreamonGCP_BinaryData)



# LICENSE

BSD 3-Clause License

Copyright (c) 2019, CME Group Inc.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of the copyright holder nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
