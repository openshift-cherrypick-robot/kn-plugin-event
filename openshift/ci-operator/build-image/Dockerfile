ARG OCP_VERSION=4.10
ARG GOLANG_VERSION=1.17
FROM registry.ci.openshift.org/ocp/${OCP_VERSION}:tools as tools

FROM registry.ci.openshift.org/ocp/builder:rhel-8-golang-${GOLANG_VERSION}-openshift-${OCP_VERSION}

COPY --from=tools /usr/bin/oc /usr/bin/
RUN ln -s /usr/bin/oc /usr/bin/kubectl
