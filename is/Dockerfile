# ------------------------------------------------------------------------
#
# Copyright 2018 WSO2, Inc. (http://wso2.com)
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License
#
# ------------------------------------------------------------------------

# set to latest Alpine
FROM mrclemrkz/wso2is:5.7
# MAINTAINER Clement Fernando "info@mrclemrkz.com”

# set user configurations
ARG USER=wso2carbon
ARG USER_HOME=/home/${USER}

# set dependant files directory
ARG CONFIG=./config

# set wso2 product configurations
ARG WSO2_SERVER=wso2is
ARG WSO2_SERVER_VERSION=5.7.0
ARG WSO2_SERVER_PACK=${WSO2_SERVER}-${WSO2_SERVER_VERSION}
ARG WSO2_SERVER_HOME=${USER_HOME}/${WSO2_SERVER_PACK}
ARG WSO2_SERVER_CONF=${WSO2_SERVER_HOME}/repository/conf

# change cofiguration
COPY --chown=wso2carbon:wso2 ${CONFIG}/tenant-mgt.xml ${WSO2_SERVER_CONF}/
COPY --chown=wso2carbon:wso2 ${CONFIG}/user-mgt.xml ${WSO2_SERVER_CONF}/
COPY --chown=wso2carbon:wso2 ${CONFIG}/carbon.xml ${WSO2_SERVER_CONF}/
