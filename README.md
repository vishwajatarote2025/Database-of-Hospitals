# Database-of-Hospitals

#include <stdio.h>
struct emergency_contacts{
    char name[10];
    int no;
    int dist;
    
};

int main() {
    int i,j;
    struct emergency_contacts em[5],temp;

        for(i=0; i<5;i++){
        
        printf("enter name of the Hospital: ");
        scanf("%s",em[i].name);
        
        printf("enter Number of the Hospital: ");
        scanf("%d",&em[i].no);
        
        printf("enter distance of that from college in meters: ");
        scanf("%d",&em[i].dist);
        printf("\n");
        }
        
        for (i=0; i<5;i++){
            for (j=i+1;j<5;j++){
                if(em[i].dist>em[j].dist){
                temp= em[i];
                em[i]=em[j];
                em[j]=temp;
                }
            
            }
        }
        printf("\nHospitals are arranged in ascending order of the distance from the college\n");
        printf("\n\n\n--------------NEAREST HOSPITALS FROM COLLEGE----------------");
        for(i=0;i<5;i++){
            printf("\n\nName of the Hospital: %s",em[i].name);
            printf("\nNumber of the Hospital: %d",em[i].no);
            printf("\nDistance of the Hospital: %d",em[i].dist);
            printf("\n---------------------------------------------------------");
        }
     return 0;
}

