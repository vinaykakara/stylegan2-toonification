# Copyright (c) 2021, NVIDIA CORPORATION.  All rights reserved.
#
# NVIDIA CORPORATION and its licensors retain all intellectual property
# and proprietary rights in and to this software, related documentation
# and any modifications thereto.  Any use, reproduction, disclosure or
# distribution of this software and related documentation without an express
# license agreement from NVIDIA CORPORATION is strictly prohibited.

FROM nvcr.io/nvidia/pytorch:20.12-py3

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install imageio-ffmpeg==0.4.3 pyspng==0.1.0

RUN apt-get update

RUN useradd vinay

COPY --chown=vinay . /home/vinay/code/

RUN chown -R vinay:vinay /home/vinay/

USER vinay

#RUN cd /home/vinay/code/ && pip3 install -r requirements.txt

WORKDIR /home/vinay/code/

