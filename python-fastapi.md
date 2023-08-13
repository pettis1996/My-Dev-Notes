# Python - FastAPI Framework Notes

## Introduction

<blockquote>
    <a href="https://fastapi.tiangolo.com/" target="_blank">
        Official Documentation
    </a>
    <p>
        <b>FastAPI</b> is a modern, fast (high-performance), web framework for building APIs with Python 3.7+ based on standard Python type hints.
    </p>
    <p>
        The key features are:
    </p>
    <ul>
        <li>
            <b>Fast:</b> Very high performance, on par with NodeJS and Go (thanks to **Starlette** and **Pydantic**). One of the fastest Python frameworks available.
        </li>
        <li>
            <b>Fast to code:</b> Increase the speed to develop features by about 200% to 300%. *
        </li>
        <li>
            <b>Fewer bugs:</b> Reduce about 40% of human (developer) induced errors. *
        </li>
        <li>    
            <b>Intuitive:</b> Great editor support. Completion everywhere. Less time debugging.
        <li>
        <li>
            <b>Easy:</b> Designed to be easy to use and learn. Less time reading docs.
        </li>
        <li>
            <b>Short:</b> Minimize code duplication. Multiple features from each parameter declaration. Fewer bugs.
        </li>
        <li>
            <b>Robust:</b> Get production-ready code. With automatic interactive documentation.
        </li>
        <li>
            <b>Standards-based:</b> Based on (and fully compatible with) the open standards for APIs: OpenAPI (previously known as Swagger) and JSON Schema.
        </li>
    </ul>
</blockquote>

<details>
    <summary>
        How to install FastAPI
    </summary>
    <br>
    <blockquote>
        <p>
            To install FastAPI you need to have python and pip installed on your machine.
        </p>
        <p>
            It is prefered to install a virtual environment for your project and install required dependencies on the virtual environment.
        </p>
        <p>
            The following guide can be used for assistance in installing venv module, creating a virtual env. and activating it.
        </p>
        <p>
            <b>Step 1: </b> Install VirtualEnv Module
        </p>
        <blockquote>
            pip install vitualenv
        </blockquote>
        <p>
            <b>Step 2:</b> Create a Virtual Env.
        </p>
        <blockquote>
            python -m venv <your-venv-name>
        </blockquote>
        <p>
            <b>Step 3:</b> Activate your Virtual Env.
        </p>
        <blockquote>
            venv/Scripts/activate
        </blockquote>
        <p>
            The pip command for installing FastAPI and all of its components:
        </p>
        <blockquote>
            pip install fastapi[all]
        </blockquote>
        <p>
            This will install all required dependencies such as uvicorn and pydantic and others.
        </p>
    </blockquote>
</details>

<details>
    <summary>
        Getting Started and Running the FastAPI Server
    </summary>
    <br>
    <blockquote>
        <p>
            First of all create an endpoint to retreive data from.
        </p>
        <blockquote>
            from fastapi import FastAPI

            app = FastAPI()


            @app.get("/")
            async def root():
                return {"message": "Hello World"}
        </blockquote>
    </blockquote>
</details>