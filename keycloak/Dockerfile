FROM quay.io/keycloak/keycloak:24.0 as builder

ENV KC_HEALTH_ENABLED=true
ENV KC_METRICS_ENABLED=true

ENV KC_CACHE_CONFIG_FILE=cache-ispn-tcpping.xml

WORKDIR /opt/keycloak

COPY cache-ispn-tcpping.xml /opt/keycloak/conf/cache-ispn-tcpping.xml

RUN /opt/keycloak/bin/kc.sh build

FROM quay.io/keycloak/keycloak:24.0
COPY --from=builder /opt/keycloak/ /opt/keycloak/