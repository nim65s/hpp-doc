ARG ROS_DISTRO=rolling
FROM ros:${ROS_DISTRO}
ARG ROS_DISTRO=rolling

WORKDIR /ws

ADD devel.repos .
RUN vcs import --input devel.repos

RUN --mount=type=cache,sharing=locked,target=/var/cache/apt \
    --mount=type=cache,sharing=locked,target=/var/lib/apt \
    apt update \
 && rosdep install --from-paths src --ignore-src -r -y

RUN . "/opt/ros/${ROS_DISTRO}/setup.sh" \
 && colcon build
