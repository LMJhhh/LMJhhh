using MEC;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using CustomPlayerEffects;
using Exiled.API.Features;
using Exiled.Events.EventArgs.Player;
using InventorySystem.Items.Usables;
using SCP_2928_ShaoMaoPlugin.SpRoles;

namespace SCP_2928_ShaoMaoPlugin
{
    internal class EventCenter
    {
        public static void RoundStarted()//表示回合开始的时候这里没有事件，至于怎么判断是什么事件往后看就行了
        {
            Timing.WaitForSeconds(0.5f);
            foreach (Player player in Player.List)//在玩家列表找玩家 因为没法写事件所以写不了变量,这里player就是变量
            {
                if (SCP_2021.shaobingmao2021.Count < 1 && Player.List.Count >= 8 && player.Role.Type == PlayerRoles.RoleTypeId.ClassD)//判定和要选择的玩家类型
                {
                    SCP_2021.烧饼猫2021(player);//这些开局就会生成2928了
                }
                else if (SCP_2021.shaobingmao639.Count < 1 && Player.List.Count >= 14 && player.Role.Type == PlayerRoles.RoleTypeId.ClassD)//判定和要选择的玩家类型
                {
                    SCP_2021.烧饼猫639(player);
                }
                else if (SCP_2021.shaobingmao237.Count < 1 && Player.List.Count >= 18 && player.Role.Type == PlayerRoles.RoleTypeId.ClassD)//判定和要选择的玩家类型
                {
                    SCP_2021.烧饼猫237(player);
                }
                else if (SCP_2928.shaobingmao2928.Count < 1 && Player.List.Count >= 18 && player.Role.Type == PlayerRoles.RoleTypeId.ClassD)//判定和要选择的玩家类型
                {
                    SCP_2928.烧饼猫2928_08(player);//这些开局就会生成2928了
                }
                else if (SCP_2928.SCP2928.Count < 1 && Player.List.Count >= 8 && player.Role.Type == PlayerRoles.RoleTypeId.FacilityGuard)//判定和要选择的玩家类型
                {
                    SCP_2928.烧饼猫2928(player);
                }
                else if (SCP_2928.SCP292824.Count < 1 && Player.List.Count >= 14 && player.Role.Type == PlayerRoles.RoleTypeId.Scientist)//判定和要选择的玩家类型
                {
                    SCP_2928.烧饼猫2928_24(player);
                }
                Timing.CallDelayed(60, () => { SCP_2928.SCP292824.Count < 1 && Player.List.Count >= 14 && player.Role.Type == PlayerRoles.RoleTypeId.Spectator;});
                    {
                        SCP_372.烧饼猫372(player);
                    }
                }
            }
        }
    }
}



<!---
LMJhhh/LMJhhh is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
