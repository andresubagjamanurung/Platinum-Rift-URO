#include <iostream>
#include <string>
#include <vector>
#include <algorithm>
#include <queue>
 
using namespace std;

int main()
{
    int jlhPemain;
    int id;
    int zone;
    int hub;
    cin >> jlhPemain >> id >> zone >> hub;
    int platinum[zone];
    for (int i = 0; i < zone; i++) {
        int zoneId;
        cin >> zoneId;
        cin >> platinum[zoneId];
    }
 
    vector <int> adjZone[zone];
    for (int i = 0; i < hub; i++) {
        int zone1;
        int zone2;
        cin >> zone1 >> zone2;
        adjZone[zone1].push_back(zone2);
        adjZone[zone2].push_back(zone1);
    }
 
    int ido[zone];
    int pod0[zone];
    int pod1[zone];
    bool visible[zone];
    int myPlat;
    int prio[zone];

    while (1) {
        cin >> myPlat; 
        for (int i = 0; i < zone; i++) {
            int zId;
            cin >> zId;
            cin >> ido[zId] >> pod0[zId] >> pod1[zId] >> visible[zId] >> platinum[zId]; cin.ignore();
 
        }
 
        for (int i = 0; i < zone; ++i) {
            if (((id == 0 && pod0[i] != 0) || (id == 1 && pod1[i] != 0))) {
                int next = adjZone[i][0];
                if (id == 0) cout << pod0[i];
                else cout << pod1[i];
                cout << ' ' << i << ' ' << next << ' ';
            }
        }
        cout << endl;
        cout << "WAIT" << endl;
    }
}
