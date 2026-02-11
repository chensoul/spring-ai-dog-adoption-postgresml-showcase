# Spring AI 狗狗领养助手展示项目

一个基于 Spring AI 的智能狗狗领养助手系统，展示了 RAG（检索增强生成）、工具调用、对话记忆等核心 AI 能力。

- 参考文章：[Your First Spring AI 1.0 Application](https://spring.io/blog/2025/05/20/your-first-spring-ai-1)
- 参考代码：[joshlong-attic/2025-05-16-anthropic](https://github.com/joshlong-attic/2025-05-16-anthropic/)

## 如何运行

```bash
git clone https://github.com/chensoul/spring-ai-dog-adoption-showcase
cd spring-ai-dog-adoption-showcase

cd scheduler
./mvnw spring-boot:run

cd ../adoptions
docker-compose up -d

export OPENAI_API_KEY=your-dashscope-api-key
./mvnw spring-boot:run
```

## 测试

```bash
# 查询可领养的狗狗
curl "http://localhost:8080/alice/assistant?question=我想领养一只金毛"

# 预约领养
curl "http://localhost:8080/alice/assistant?question=我想预约领养Buddy"
```