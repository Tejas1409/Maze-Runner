/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package Algorithms;

import java.util.ArrayList;
import java.util.List;

/**
 *
 * @author Shrenik
 */
public class DFS {
    public static boolean searchPath(int[][]maze, int x, int y, List<Integer>path){
      if(maze[x][y]==9){
          return true;
      }
      if(maze[x][y]==0){
          maze[x][y]=2;
          
          int[]dx = {1, 0, -1, 0};
          int[]dy = {0, -1, 0, 1};
          
          for(int d=0; d<4; d++){
             int newX = x + dx[d];
             int newY = y + dy[d];
             
             if(newX>=0 && newY>=0 && newX<maze.length && newY<maze[0].length && searchPath(maze,newX,newY, path)){
                 System.out.println(newX + ","+newY);
                 path.add(x);
                 path.add(y);
                 return true;
             }
          }
      }
      return false;
    }
    public static void main(String[] args){
        DFS obj = new DFS();
        int[][]maze = {
            {0, 0, 1},
            {0, 1, 9},
            {0, 0, 0},
        };
        List<Integer>path = new ArrayList<Integer>();
        boolean reach = obj.searchPath(maze, 0, 0, path);
        System.out.println(reach);
    }
}
