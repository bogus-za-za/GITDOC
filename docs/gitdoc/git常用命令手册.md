# Git 常用命令手册

## 1. 仓库操作
```bash title="查看版本"
git -v
```
```bash title="初始化本地仓库"
git init
```
## 2.基本配置

:::tip

`--global` 表示全局配置 不携带表示在当前项目

:::

```bash title="配置用户名"
git config --global user.name "这宣传"
```


```bash title="配置邮箱"
git config --global user.email "1321@163.com"
```

## 3.新建仓库

```bash title="初始化仓库"
git init
```

```bash title="初始化仓库携带目录my-repo"
git init my-repo
```
:::tip

使用 `git clone` 时需注意选择连接方式，推荐使用 `ssh` 

:::

```bash title="克隆远程仓库"
git clone url
```

## 4.流程操作
:::tip

使用 `git ls-files` 查看暂存区

:::

```bash title="添加入暂存区"
git add 文件名
```

```bash title="查看状态"
git status
```

:::tip

使用 `git commit` 时只会提交暂存区内的文件，如果文件属于未跟踪状态则不提交

:::

```bash title="提交"
git commit
```
:::tip

参数 `--one line` 表示简洁信息

:::

```bash title="显示信息"
git log
```

## 5.回退版本

:::tip

 参数`--soft` 表示简洁信息、参数`--hard` 表示简洁信息、参数`--mixed` 表示混合、
 

:::



import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="soft" label="soft" default>
    表示回退到某一个版本，并保留工作区和暂存区的所有修改内容
  </TabItem>
  <TabItem value="hard" label="hard">
    表示回退到某一个版本，并丢弃工作区和暂存区的所有修改内容
  </TabItem>
  <TabItem value="mixed" label="mixed">
    表示回退到某一个版本，并保留工作区的所有修改内容，丢弃暂存区的所有修改内容
  </TabItem>
</Tabs>


```bash title="回退版本"
git reset --soft
```

## 6.查看差异




<Tabs>
<TabItem value="soft" label="soft" default>
```jsx

$ git diff
warning: in the working copy of 'file2.txt', LF will be replaced by CRLF the next time Git touches it

/* 表示变更文件 */
diff --git a/file2.txt b/file2.txt
index c200906..20c6f0a 100644
--- a/file2.txt
+++ b/file2.txt
@@ -1 +1 @@
-222
+ces 

```

</TabItem>

<TabItem value="hard" label="hard">

```jsx

$ git diff
warning: in the working copy of 'file2.txt', LF will be replaced by CRLF the next time Git touches it

/* 表示变更文件 */
diff --git a/file2.txt b/file2.txt
index c200906..20c6f0a 100644
--- a/file2.txt
+++ b/file2.txt
@@ -1 +1 @@
-222
+ces 

```
</TabItem>
<TabItem value="mixed" label="mixed">
```jsx

$ git diff
warning: in the working copy of 'file2.txt', LF will be replaced by CRLF the next time Git touches it

/* 表示变更文件 */
diff --git a/file2.txt b/file2.txt
index c200906..20c6f0a 100644
--- a/file2.txt
+++ b/file2.txt
@@ -1 +1 @@
-222
+ces 

```
</TabItem>
</Tabs>

```bash title="回退版本"
git diff
```
|编号|参数|使用方式|
| ----------- | ----------- | ----------- |
| 1 | `123` | zxc |
| 2 | zxcz | zxc |
| 3 | zxcz | zxc |
| 4 | zxcz | zxc |

