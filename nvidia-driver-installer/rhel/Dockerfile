# Copyright 2021 Google Inc. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

ARG base_image=registry.access.redhat.com/ubi7:7.9-405

FROM ${base_image}

RUN yum update -y && \
    yum install -y gcc make && \
		yum clean all && \
		rm -rf /var/cache/yum

COPY entrypoint.sh /entrypoint.sh

CMD /entrypoint.sh
