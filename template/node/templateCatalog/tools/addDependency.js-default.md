const fs = require('fs-extra');

const packageSource = process.env.PACKAGE_SOURCE;
const packageJsonPath = './test/realProject/package.json';
const packageJson = fs.readJsonSync(packageJsonPath);
packageJson.dependencies = {"s-update-manager": `../.${packageSource}`};
fs.writeJsonSync(packageJsonPath, packageJson, { spaces: 2 });

console.log('realProject prepared to test package');
