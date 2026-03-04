# Anthony Fu's Skills

A curated collection of [Agent Skills](https://agentskills.io/home) reflecting [Anthony Fu](https://github.com/antfu)'s preferences, experience, and best practices, along with usage documentation for the tools.

> [!IMPORTANT]
> This is a proof-of-concept project for generating agent skills from source documentation and keeping them in sync.
> I haven't fully tested how well the skills perform in practice, so feedback and contributions are greatly welcome.

## Installation

```bash
pnpx skills add antfu/skills --skill='*'
### **Anthony Fu 的技能集**

这是一个由 Anthony Fu 整理的 Agent Skills 精选集合，反映了他的偏好、经验和最佳实践，同时包含了工具的使用文档。

**重要提示**

这是一个从源文档生成 Agent Skills 并保持同步的概念验证项目。我还没有完全测试这些技能在实际使用中的表现，因此非常欢迎反馈和贡献。

## **安装**

```
pnpx skills add antfu/skills --skill='*'
```

或者全局安装所有技能：

```
pnpx skills add antfu/skills --skill='*' -g
```

更多关于 CLI 用法的信息，请访问 skills。

## **技能**

这个集合旨在成为主要使用 Vite/Nuxt 工作的一站式技能集合。它包含了来自不同来源、不同范围的技能。

### **手动维护的技能**

> 有特定观点

由 Anthony Fu 手动维护，包含他偏好的工具、设置约定和最佳实践。

---

技能 | 描述
--- | ---
antfu | Anthony Fu 对应用/库项目的偏好和最佳实践（eslint、pnpm、vitest、vue 等）

### **从官方文档生成的技能**

> 无特定观点但有所侧重（例如 TypeScript、ESM、Composition API 和其他现代技术栈）

从官方文档生成并由 Anthony 微调。

---

技能 | 描述 | 来源
--- | --- | ---
vue | Vue.js 核心 - 响应式、组件、组合式 API | vuejs/docs
nuxt | Nuxt 框架 - 基于文件的路由、服务器路由、模块 | nuxt/nuxt
pinia | Pinia - 直观、类型安全的 Vue 状态管理 | vuejs/pinia
vite | Vite 构建工具 - 配置、插件、SSR、库模式 | vitejs/vite
vitepress | VitePress - 由 Vite 驱动的静态站点生成器 | vuejs/vitepress
vitest | Vitest - 由 Vite 驱动的单元测试框架 | vitest-dev/vitest
unocss | UnoCSS - 原子化 CSS 引擎、预设、转换器 | unocss/unocss
pnpm | pnpm - 快速、磁盘空间高效的包管理器 | pnpm/pnpm.io

### **第三方技能**

从维护自己技能的外部仓库同步而来。

---

技能 | 描述 | 来源
--- | --- | ---
slidev (官方) | Slidev - 面向开发者的演示文稿幻灯片 | slidevjs/slidev
tsdown (官方) | tsdown - 由 Rolldown 驱动的 TypeScript 库打包工具 | rolldown/tsdown
turborepo (官方) | Turborepo - 面向 monorepo 的高性能构建系统 | vercel/turborepo
vueuse-functions (官方) | VueUse - 200+ Vue 组合式工具函数 | vueuse/skills
vue-best-practices | Vue 3 + TypeScript 最佳实践 | vuejs-ai/skills
vue-router-best-practices | Vue Router 最佳实践 | vuejs-ai/skills
vue-testing-best-practices | Vue 测试最佳实践 | vuejs-ai/skills
web-design-guidelines | 构建美观界面的网页设计指南 | vercel-labs/agent-skills

## **常见问题**

### **这个集合有什么不同之处？**

这个集合有特定观点，但关键区别在于它使用 git 子模块直接引用源文档。这提供了更可靠的上下文，并允许技能随着时间的推移与上游变更保持同步。如果您主要使用 Vue/Vite/Nuxt 工作，这旨在成为一个全面的一站式集合。

该项目还设计得很灵活 - 您可以将其作为模板来生成自己的技能集合。

### **Skills 与 llms.txt 与 AGENTS.md**

对我来说，Skills 的价值在于**可共享**和**按需使用**。

可共享使得提示更容易跨项目管理重用。按需使用意味着技能可以根据需要引入，远远超出了任何 Agent 上下文窗口一次能容纳的范围。

您可能听说过 "AGENTS.md 优于 skills"。我认为这是真的 — AGENTS.md 会预先加载所有内容，因此 Agent 总是会遵守它，而 skills 可能会出现误判，即 Agent 在您期望的时候没有引入它们。话虽如此，我认为这更多是工具和集成的差距，随着时间的推移会有所改善。Skills 实际上只是 Agent 消费的标准化格式 - 归根结底是纯 Markdown 文件。将它们视为 Agent 的知识库。如果您希望某些技能始终适用，可以直接在 AGENTS.md 中引用它们。

## **生成您自己的技能**

Fork 这个项目来创建您自己定制的技能集合。

1. Fork 或克隆此仓库
2. 安装依赖：`pnpm install`
3. 使用您自己的项目和技能源更新 `meta.ts`
4. 运行 `pnpm start cleanup` 以移除现有的子模块和技能
5. 运行 `pnpm start init` 以克隆子模块
6. 运行 `pnpm start sync` 以同步第三方技能
7. 让您的 Agent `为 <项目> 生成技能`（建议一次一个，以管理 token 使用量）

有关详细的生成指南，请参阅 AGENTS.md。

## **赞助商**

## **许可证**

此仓库中的技能和脚本采用 MIT 许可证。

来自外部仓库的第三方技能保留其原始许可证 - 详情请参阅每个技能目录。

## **关于**

Anthony Fu 整理的 Agent Skills 精选集合。

### **资源**

Readme

### **许可证**

MIT 许可证

### **星标**

**0** 个星标

### **关注者**

**0** 个关注者

### **分支**

**0** 个分支

## **发布**

没有发布版本

创建新发布

## **包**

没有发布的包

发布您的第一个包

## **贡献者**

没有贡献者

## **语言**

- TypeScript 99.1%
- JavaScript 0.9%





























































































or to install all of them globally:

```bash
pnpx skills add antfu/skills --skill='*' -g
```

Learn more about the CLI usage at [skills](https://github.com/vercel-labs/skills).

## Skills

This collection is aim to be a one-stop collection of you are mainly working on Vite/Nuxt. It includes skills from different sources with different scopes.

### Hand-maintained Skills

> Opinionated

Manually maintained by Anthony Fu with his preferred tools, setup conventions, and best practices.

| Skill | Description |
|-------|-------------|
| [antfu](skills/antfu) | Anthony Fu's preferences and best practices for app/library projects (eslint, pnpm, vitest, vue, etc.) |

### Skills Generated from Official Documentation

> Unopinionated but with tilted focus (e.g. TypeScript, ESM, Composition API, and other modern stacks)

Generated from official documentation and fine-tuned by Anthony.

| Skill | Description | Source |
|-------|-------------|--------|
| [vue](skills/vue) | Vue.js core - reactivity, components, composition API | [vuejs/docs](https://github.com/vuejs/docs) |
| [nuxt](skills/nuxt) | Nuxt framework - file-based routing, server routes, modules | [nuxt/nuxt](https://github.com/nuxt/nuxt) |
| [pinia](skills/pinia) | Pinia - intuitive, type-safe state management for Vue | [vuejs/pinia](https://github.com/vuejs/pinia) |
| [vite](skills/vite) | Vite build tool - config, plugins, SSR, library mode | [vitejs/vite](https://github.com/vitejs/vite) |
| [vitepress](skills/vitepress) | VitePress - static site generator powered by Vite | [vuejs/vitepress](https://github.com/vuejs/vitepress) |
| [vitest](skills/vitest) | Vitest - unit testing framework powered by Vite | [vitest-dev/vitest](https://github.com/vitest-dev/vitest) |
| [unocss](skills/unocss) | UnoCSS - atomic CSS engine, presets, transformers | [unocss/unocss](https://github.com/unocss/unocss) |
| [pnpm](skills/pnpm) | pnpm - fast, disk space efficient package manager | [pnpm/pnpm.io](https://github.com/pnpm/pnpm.io) |

### Vendored Skills

Synced from external repositories that maintain their own skills.

| Skill | Description | Source |
|-------|-------------|--------|
| [slidev](skills/slidev) (Official) | Slidev - presentation slides for developers | [slidevjs/slidev](https://github.com/slidevjs/slidev) |
| [tsdown](skills/tsdown) (Official) | tsdown - TypeScript library bundler powered by Rolldown | [rolldown/tsdown](https://github.com/rolldown/tsdown) |
| [turborepo](skills/turborepo) (Official) | Turborepo - high-performance build system for monorepos | [vercel/turborepo](https://github.com/vercel/turborepo) |
| [vueuse-functions](skills/vueuse-functions) (Official) | VueUse - 200+ Vue composition utilities | [vueuse/skills](https://github.com/vueuse/skills) |
| [vue-best-practices](skills/vue-best-practices) | Vue 3 + TypeScript best practices | [vuejs-ai/skills](https://github.com/vuejs-ai/skills) |
| [vue-router-best-practices](skills/vue-router-best-practices) | Vue Router best practices | [vuejs-ai/skills](https://github.com/vuejs-ai/skills) |
| [vue-testing-best-practices](skills/vue-testing-best-practices) | Vue testing best practices | [vuejs-ai/skills](https://github.com/vuejs-ai/skills) |
| [web-design-guidelines](skills/web-design-guidelines) | Web design guidelines for building beautiful interfaces | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) |

## FAQ

### What Makes This Collection Different?

This collection is opinionated, but the key difference is that it uses git submodules to directly reference source documentation. This provides more reliable context and allows the skills to stay up-to-date with upstream changes over time. If you primarily work with Vue/Vite/Nuxt, this aims to be a comprehensive one-stop collection.

The project is also designed to be flexible - you can use it as a template to generate your own skills collection.

### Skills vs llms.txt vs AGENTS.md

To me, the value of skills lies in being **shareable** and **on-demand**.

Being shareable makes prompts easier to manage and reuse across projects. Being on-demand means skills can be pulled in as needed, scaling far beyond what any agent's context window could fit at once.

You might hear people say "AGENTS.md outperforms skills". I think that's true — AGENTS.md loads everything upfront, so agents always respect it, whereas skills can have false negatives where agents don't pull them in when you'd expect. That said, I see this more as a gap in tooling and integration that will improve over time. Skills are really just a standardized format for agents to consume—plain markdown files at the end of the day. Think of them as a knowledge base for agents. If you want certain skills to always apply, you can reference them directly in your AGENTS.md.

## Generate Your Own Skills

Fork this project to create your own customized skill collection.

1. Fork or clone this repository
2. Install dependencies: `pnpm install`
3. Update `meta.ts` with your own projects and skill sources
4. Run `pnpm start cleanup` to remove existing submodules and skills
5. Run `pnpm start init` to clone the submodules
6. Run `pnpm start sync` to sync vendored skills
7. Ask your agent to `Generate skills for \<project\>` (recommended one at a time to manage token usage)

See [AGENTS.md](AGENTS.md) for detailed generation guidelines.

## Sponsors

<p align="center">
  <a href="https://cdn.jsdelivr.net/gh/antfu/static/sponsors.svg">
    <img src='https://cdn.jsdelivr.net/gh/antfu/static/sponsors.svg'/>
  </a>
</p>

## License

Skills and the scripts in this repository are [MIT](LICENSE.md) licensed.

Vendored skills from external repositories retain their original licenses - see each skill directory for details.
