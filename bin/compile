#!/usr/bin/env bash
# bin/compile <build-dir> <cache-dir> <env-dir>

BUILD_DIR=${1:-}
CACHE_DIR=${2:-}
ENV_DIR=${3:-}

echo "------> Generating .profile.d file to generate google-credentials.json at startup"
mkdir -p $BUILD_DIR/.profile.d
CREDENTIALS=$(cat ${ENV_DIR}/GOOGLE_CREDENTIALS)
echo "echo ${CREDENTIALS@Q} > /app/google-credentials.json" > $BUILD_DIR/.profile.d/google-credentials.sh
chmod +x $BUILD_DIR/.profile.d/google-credentials.sh
