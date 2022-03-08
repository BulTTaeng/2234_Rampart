# 2234_Rampart

made by Jaehyeok Choi

## Welcome to Jaehyeok's github!

## What is the problem?

![image](https://github.com/Choi-JaeHyeok-21500749/2234_Rampart/blob/main/2234_pro.PNG)

## What Algorithm should I use?

Graph Algorithm , dfs

## What was the key point and the hard part?

The first answer and second answer is easy to think. 

Just doing search(bfs or dfs) and count the not -visited location and if some location is not visited , raise the number of room and do dfs again.

Repeat this (0,0) to (N-1, M-1) will work.

For the third answer, I though make visit array 3d and do search with information that I break wall or not, but because we just want to know the max size,
just searching from (0,0) to (N-1 , M-1) and search NWES will work if we save the room size and and fill visit with diffrent number.

When checking there is a wall or not , I write every case with if-else statement , but I found in the internet when we use & operator , this can be easy and shorter.

        int Wall = 1;
 
        for (int i = 0; i < 4; i++)
        {
            if ((MAP[x][y] & Wall) != Wall)
            {
                int nx = x + dx[i];
                int ny = y + dy[i];
 
                if (nx >= 0 && ny >= 0 && nx < N && ny < M)
                {
                    if (Visit[nx][ny] == false)
                    {
                        Room_Size++;
                        Visit[nx][ny] = true;
                        Q.push(make_pair(nx, ny));
                    }
                }
            }
            Wall = Wall * 2;
        }


출처: https://yabmoons.tistory.com/59 [얍문's Coding World..]


## Where can I get more help, if I need it?

You can contact me through email, which is wogur7496@gmail.com.
Thank you for visiting this github!
