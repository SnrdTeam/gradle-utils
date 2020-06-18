# gradle-utils

Набор подключаемых модулей Gradle.

Модули:

  * project-extensions
  * java-extensions
  * ossrh-extensions
  * dependency-licenses

## project-extensions

Утилиты для работы с экземпляром класса `org.gradle.Project`.

### Использование

В файле .gradle добавьте

```groovy
apply from: 'https://raw.githubusercontent.com/SnrdTeam/gradle-utils/master/project-extensions.gradle'
```

## java-extensions

Утилиты для работы с плагином Java.

### Использование

В файле .gradle добавьте

```groovy
apply from: 'https://raw.githubusercontent.com/SnrdTeam/gradle-utils/master/java-extensions.gradle'
```

## ossrh-extensions

Утилиты для работы с плагинами для публикации артефактов в Maven: `maven`,`io.codearte.gradle.nexus.NexusStagingPlugin`.

### Использование

В файле .gradle добавьте

```groovy
apply from: 'https://raw.githubusercontent.com/SnrdTeam/gradle-utils/master/ossrh-publish.gradle'
```

## dependency-licenses

Утилиты для проверки лицензий сторонних библиотек, подключенных в качестве зависимостей проекта.

### Использование

В файле .gradle добавьте

```groovy
apply from: 'https://raw.githubusercontent.com/SnrdTeam/gradle-utils/dependency-licenses-v1.0/dependency-licenses.gradle'
createCheckDependencyLicensesTask(project.file('/src/main/res/raw/licenses.json'))
preBuild.dependsOn checkDependencyLicenses
```

## Лицензия

Copyright 2017 Adeptik

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.