# GitHub Actions

GitHub 推出的持續整合(CI)解決方案

![「檢查專案中的潛在問題」GitHub Actions 作業流程狀態標章](https://github.com/libre-knowledge/github-actions/actions/workflows/check-potential-problems.yml/badge.svg "本專案使用 GitHub Actions 自動化檢查專案中的潛在問題") [![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white  "本專案使用 pre-commit 檢查專案中的潛在問題")](https://github.com/pre-commit/pre-commit) [![REUSE 規範遵從狀態標章](https://api.reuse.software/badge/github.com/libre-knowledge/github-actions "本專案遵從 REUSE 規範降低軟體授權成本")](https://api.reuse.software/info/github.com/libre-knowledge/github-actions)

## 基本概念

### 動作<br>Action

* 一個可以作到某個操作的可調用工具
* 可以使用第三方或是自己開發的[動作](#Action)

### 步驟<br>Step

* 一個持續整合單位，每個[步驟](#步驟step)皆調用一個[動作](#動作action)或是一個 shell 命令去做一件事情

### 工作<br>Job

* 完成一件有意義的事情之有順序性[步驟](#步驟step)的集合
* 預設情況下一[工作](#工作job)可與其他[工作](#工作job)平行運行，但也可以設定[工作](#工作job)間的依賴關係(dependency)讓一[工作](#工作job)在另一[工作](#工作job)完成後才運行

### 工作流程<br>Workflow

* 一個可以整合到專案之自動化程序，定義一或多個[工作](#工作job)的持續整合單位
* 一個[工作流程](#工作流程workflow)可以參照並調用另一[工作流程](#工作流程workflow)，提高代碼可重複利用性(reusability)

### 事件<br>Event

可以用來觸發(trigger)一[工作流程](#工作流程workflow)的事件，包含但不限於：

* pull
* tag
* fork

所有可用之[事件](#事件event)請參閱 [Events that trigger workflows - GitHub Docs](https://docs.github.com/en/actions/learn-github-actions/events-that-trigger-workflows) 官方文件的說明

### 執行器<br>Runner

* 一個運行了 [GitHub Actions 執行器應用](https://github.com/actions/runner)，[用來執行各個[工作](#工作job)的運算節點，可以[由 GitLab 提供](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners)（有使用時間等限制）也可以[自己架設](https://docs.github.com/en/actions/hosting-your-own-runners)（可客製程度較大）
* 一[工作](#工作job)只會在一[執行器](#執行器runner)中運行，同一[工作](#工作job)中的[步驟](#步驟step)可以共享資料

## 參考資料

* [Features • GitHub Actions](https://github.com/features/actions)  
  官方網頁
* [GitHub Actions Documentation - GitHub Docs](https://docs.github.com/en/actions)  
  官方說明文件
* [Events that trigger workflows - GitHub Docs](https://docs.github.com/en/actions/learn-github-actions/events-that-trigger-workflows)
* [actions/runner: The Runner for GitHub Actions](https://github.com/actions/runner)
* [About GitHub-hosted runners - GitHub Docs](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners)
* [Hosting your own runners - GitHub Docs](https://docs.github.com/en/actions/hosting-your-own-runners)
* [Workflow syntax for GitHub Actions - GitHub Docs](https://docs.github.com/en/actions/learn-github-actions/workflow-syntax-for-github-actions)  
  工作流程定義檔的語法參考
