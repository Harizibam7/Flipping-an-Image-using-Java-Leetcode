# Flipping-an-Image-using-Java-Leetcode\

    class Solution {
        public int[][] flipping(int[][] images){
            int[][] img = new int[images.length][images.length];
            for(int i =0; i<images.length;i++){
                int[] arr= notreverse(images[i],images[i].length);
                for(int j =0;j<images.length;j++){
                    img[i][j] = arr[j];
                }
            }
            return img;
        }   
        public int[] notreverse(int[] image,int n){
            int[] arr = new int[n];
            int j =n-1;
            for(int i =0; i< image.length;i++){
                int temp = image[j]==0?1:0;
                arr[i] = temp;
                j--;
            }
            return arr;
        }
        public int[][] flipAndInvertImage(int[][] image) {
            return flipping(image);
        }
    }
