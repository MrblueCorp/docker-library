FROM docker:20.10.22

###############################################################
# CI/CD 필요한 유틸리티 설치
# curl, bash, Node.js, pnpm(corepack에 포함 되는것으로 보임)
###############################################################

RUN apk --no-cache add --update bash curl nodejs npm

RUN npm install -g corepack \
    && corepack enable

RUN curl --help && cat /etc/shells \
    && echo node : $(node -v) \
    && echo npm : $(npm -v) \
    && echo pnpm : $(pnpm -v)


ENTRYPOINT ["docker-entrypoint.sh"]
