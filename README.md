# reflection-agent

reflection-style agent architecture built with LangGraph that improves output quality through self-critique and refinement.

I'm learning to use [LangGraph](https://www.langchain.com/langgraph)l by taking a [Udemy class](https://www.udemy.com/course/langgraph)

``` mermaid
graph TD;
        __start__([<p>__start__</p>]):::first
        generate(generate)
        reflect(reflect)
        __end__([<p>__end__</p>]):::last
        __start__ --> generate;
        generate -.-> __end__;
        generate -.-> reflect;
        reflect --> generate;
        classDef default fill:#f2f0ff,line-height:1.2
        classDef first fill-opacity:0
        classDef last fill:#bfb6fc
```

Note that you'll need an `.env` file like this:

``` text
OPENAI_API_KEY=<MY_OPENAI_API_KEY>
LANGCHAIN_API_KEY=<MY_LANGSMITH_API_KEY>
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=reflection agent
```
