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

TAG?=latest
REGISTRY?=docker.io
IMAGE=rhel-nvidia-driver-installer

container:
	docker build --build-arg base_image=registry.access.redhat.com/ubi7:7.9-405 --pull -t ${REGISTRY}/${IMAGE}:7-${TAG} -t ${REGISTRY}/${IMAGE}:${TAG} .
	docker build --build-arg base_image=registry.access.redhat.com/ubi8:8.4-203.1622660121 --pull -t ${REGISTRY}/${IMAGE}:8-${TAG} .

push:
	docker push ${REGISTRY}/${IMAGE}:${TAG}
	docker push ${REGISTRY}/${IMAGE}:7-${TAG}
	docker push ${REGISTRY}/${IMAGE}:8-${TAG}

.PHONY: container push
