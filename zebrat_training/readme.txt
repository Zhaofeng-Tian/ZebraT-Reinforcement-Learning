

#### start_training.py ####
env = StartOpenAI_ROS_Environment (task_and_robot_environment_name)

----------->>>

#### openai_ros_common.py ####

Call ----->>> class StartOpenAI_ROS_Environment (task_and_robot_environment_name)
Call class function ----->>>  



####  task_envs_list.py ####

------>>>> RegisterOpenAI_Ros_Env(task_env, max_episode_steps=10000)
------>>>> gym.env

start_training.py 寻找人物环境id 
ros_common中 调用 task_envs_list 中函数
list 由id找到 zebrat_wall 中的 ZebratWallEnv
返回true, 然后make环境
env <<<<------ZebratWallEnv (which继承ZebratEnv的函数和变量)
start_traning call env.step(action)
----> env._set_action
----> env.move_base
 ....
----> time.sleep(0.2)
step中 gazebbo.pauseSim()
get (obs, reward = _compute_reward, done, info)

return obs, reward, done, info