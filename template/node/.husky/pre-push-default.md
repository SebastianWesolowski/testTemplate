#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

echo \[🐶 Husky] Running pre-push hook...\

yarn husky:pre-push

echo \[🐶 Husky] Done ✅ pre-push hook...\
