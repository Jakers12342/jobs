# jobs
--[[---------------------------------------------------------------------------
DarkRP custom jobs
---------------------------------------------------------------------------

This file contains your custom jobs.
This file should also contain jobs from DarkRP that you edited.

Note: If you want to edit a default DarkRP job, first disable it in darkrp_config/disabled_defaults.lua
	Once you've done that, copy and paste the job to this file and edit it.

The default jobs can be found here:
https://github.com/FPtje/DarkRP/blob/master/gamemode/config/jobrelated.lua

For examples and explanation please visit this wiki page:
http://wiki.darkrp.com/index.php/DarkRP:CustomJobFields


Add jobs under the following line:
---------------------------------------------------------------------------]]
TEAM_CITIZEN = DarkRP.createJob("Citizen", {
    color = Color(20, 150, 20, 255),
    model = {
        "models/player/Group01/Female_01.mdl",
        "models/player/Group01/Female_02.mdl",
        "models/player/Group01/Female_03.mdl",
        "models/player/Group01/Female_04.mdl",
        "models/player/Group01/Female_06.mdl",
        "models/player/group01/male_01.mdl",
        "models/player/Group01/Male_02.mdl",
        "models/player/Group01/male_03.mdl",
        "models/player/Group01/Male_04.mdl",
        "models/player/Group01/Male_05.mdl",
        "models/player/Group01/Male_06.mdl",
        "models/player/Group01/Male_07.mdl",
        "models/player/Group01/Male_08.mdl",
        "models/player/Group01/Male_09.mdl"
    },
    description = [[The Citizen is the most basic level of society you can hold besides being a hobo. You have no specific role in city life.]],
    weapons = {"weapon_fists"},
    command = "citizen",
    max = 0,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    candemote = false,
    category = "Citizens",
})

TEAM_SWAT = DarkRP.createJob("Swat", {
    color = Color(25, 25, 170, 255),
    model = {"models/player/swat.mdl"},
    description = [[The protector of every citizen that lives in the city.
        You have the power to arrest criminals and protect innocents.
        Hit a player with your arrest baton to put them in jail.
        Bash a player with a stunstick and they may learn to obey the law.
        The Battering Ram can break down the door of a criminal, with a warrant for their arrest.
        The Battering Ram can also unfreeze frozen props (if enabled).
        Type /wanted <name> to alert the public to the presence of a criminal.]],
    weapons = {"arrest_stick", "unarrest_stick", "m9k_m92beretta", "stunstick", "door_ram", "weaponchecker", "m9k_deagle", "m9k_magpulpdr"},
    command = "Swat",
    max = 4,
    salary = 85,
    admin = 0,
    vote = true,
    hasLicense = true,
    help = {
        "Please don't abuse your job",
        "When you arrest someone they are auto transported to jail.",
        "They are auto let out of jail after some time",
        "Type /warrant [Nick|SteamID|Status ID] to set a search warrant for a player.",
        "Type /wanted [Nick|SteamID|Status ID] to alert everyone to a wanted suspect",
        "Type /unwanted [Nick|SteamID|Status ID] to clear the suspect",
        "Type /jailpos to set the jail position"
    },
    category = "Civil Protection",
})

TEAM_SWATL = DarkRP.createJob("Swat Leader", {
    color = Color(25, 25, 170, 255),
    model = {"models/player/swat.mdl"},
    description = [[The protector of every citizen that lives in the city.
        You have the power to arrest criminals and protect innocents.
        Hit a player with your arrest baton to put them in jail.
        Bash a player with a stunstick and they may learn to obey the law.
        The Battering Ram can break down the door of a criminal, with a warrant for their arrest.
        The Battering Ram can also unfreeze frozen props (if enabled).
        Type /wanted <name> to alert the public to the presence of a criminal.]],
    weapons = {"arrest_stick", "unarrest_stick", "m9k_m92beretta", "stunstick", "door_ram", "weaponchecker", "m9k_deagle", "m9k_magpulpdr"},
    command = "SwatLeader",
    max = 1,
    salary = 85,
    admin = 0,
    vote = true,
    hasLicense = true,
    help = {
        "Please don't abuse your job",
        "When you arrest someone they are auto transported to jail.",
        "They are auto let out of jail after some time",
        "Type /warrant [Nick|SteamID|Status ID] to set a search warrant for a player.",
        "Type /wanted [Nick|SteamID|Status ID] to alert everyone to a wanted suspect",
        "Type /unwanted [Nick|SteamID|Status ID] to clear the suspect",
        "Type /jailpos to set the jail position"
    },
    category = "Civil Protection",
})

TEAM_SECRET = DarkRP.createJob("Secret Service", {
    color = Color(255, 102, 102, 255),
    model = "models//player/ct_gsg9.mdl",
    description = [[Protect the Mayor at all costs]],
    weapons = {"arrest_stick", "unarrest_stick", "m9k_m92beretta", "stunstick", "door_ram", "weaponchecker", "m9k_mp9"},
    command = "secretservice",
    max = 2,
    salary = 65,
    admin = 0,
    vote = true,
    hasLicense = true,
    category = "Civil Protection",
})

TEAM_MEDDY = DarkRP.createJob("SWAT Medic", {
    color = Color(0, 0, 255, 255),
    model = "models/player/ct_gign.mdl",
    description = [[Heal your SWAT bretheren]],
    weapons = {"med_kit"},
    command = "swatmed",
    max = 2,
    salary = 65,
    admin = 0,
    vote = true,
    hasLicense = true,
    category = "Civil Protection",
})

TEAM_POLICE = DarkRP.createJob("Police", {
    color = Color(25, 25, 170, 255),
    model = {"models/player/police.mdl", "models/player/police_fem.mdl"},
    description = [[The protector of every citizen that lives in the city.
        You have the power to arrest criminals and protect innocents.
        Hit a player with your arrest baton to put them in jail.
        Bash a player with a stunstick and they may learn to obey the law.
        The Battering Ram can break down the door of a criminal, with a warrant for their arrest.
        The Battering Ram can also unfreeze frozen props (if enabled).
        Type /wanted <name> to alert the public to the presence of a criminal.]],
    weapons = {"arrest_stick", "unarrest_stick", "weapon_glock2", "stunstick", "door_ram", "weaponchecker"},
    command = "cp",
    max = 4,
    salary = GAMEMODE.Config.normalsalary * 1.45,
    admin = 0,
    vote = true,
    hasLicense = true,
    ammo = {
        ["pistol"] = 60,
    },
    category = "Civil Protection",
})

TEAM_MEDIC = DarkRP.createJob("Medic", {
    color = Color(47, 79, 79, 255),
    model = "models/player/kleiner.mdl",
    description = [[With your medical knowledge you work to restore players to full health.
        Without a medic, people cannot be healed.
        Left click with the Medical Kit to heal other players.
        Right click with the Medical Kit to heal yourself.]],
    weapons = {"med_kit"},
    command = "medic",
    max = 3,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    medic = true,
    category = "Citizens",
})

TEAM_CHIEF = DarkRP.createJob("Police Cheif", {
    color = Color(20, 20, 255, 255),
    model = "models/player/combine_soldier_prisonguard.mdl",
    description = [[The Chief is the leader of the Civil Protection unit.
        Coordinate the police force to enforce law in the city.
        Hit a player with arrest baton to put them in jail.
        Bash a player with a stunstick and they may learn to obey the law.
        The Battering Ram can break down the door of a criminal, with a warrant for his/her arrest.
        Type /wanted <name> to alert the public to the presence of a criminal.
        Type /jailpos to set the Jail Position]],
    weapons = {"arrest_stick", "unarrest_stick", "weapon_deagle2", "stunstick", "door_ram", "weaponchecker"},
    command = "chief",
    max = 1,
    salary = GAMEMODE.Config.normalsalary * 1.67,
    admin = 0,
    vote = false,
    hasLicense = true,
    chief = true,
    NeedToChangeFrom = TEAM_POLICE,
    ammo = {
        ["pistol"] = 60,
    },
    category = "Civil Protection",
})

TEAM_MAYOR = DarkRP.createJob("Mayor", {
    color = Color(150, 20, 20, 255),
    model = "models/player/breen.mdl",
    description = [[The Mayor of the city creates laws to govern the city.
    If you are the mayor you may create and accept warrants.
    Type /wanted <name>  to warrant a player.
    Type /jailpos to set the Jail Position.
    Type /lockdown initiate a lockdown of the city.
    Everyone must be inside during a lockdown.
    The cops patrol the area.
    /unlockdown to end a lockdown]],
    weapons = {},
    command = "mayor",
    max = 1,
    salary = GAMEMODE.Config.normalsalary * 1.89,
    admin = 0,
    vote = true,
    hasLicense = false,
    mayor = true,
    category = "Civil Protection",
})

TEAM_LIGHTDEALER = DarkRP.createJob("LightGun Dealer", {
    color = Color(255, 140, 0, 255),
    model = "models/player/monk.mdl",
    description = [[A Gun Dealer is the only person who can sell guns to other people.
        Make sure you aren't caught selling illegal firearms to the public! You might get arrested!]],
    weapons = {},
    command = "lightdealer",
    max = 2,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "GunDealers",
})

TEAM_HEAVYDEALER = DarkRP.createJob("HeavyGun Dealer", {
    color = Color(255, 140, 0, 255),
    model = "models/player/monk.mdl",
    description = [[A Gun Dealer is the only person who can sell guns to other people.
        Make sure you aren't caught selling illegal firearms to the public! You might get arrested!]],
    weapons = {},
    command = "heavydealer",
    max = 2,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "GunDealers",
})

TEAM_BLACKMARKETDEALER = DarkRP.createJob("BlackMarket Dealer", {
    color = Color(255, 140, 0, 255),
    model = "models/player/monk.mdl",
    description = [[A Gun Dealer is the only person who can sell guns to other people.
        Make sure you aren't caught selling illegal firearms to the public! You might get arrested!]],
    weapons = {},
    command = "blackmarketgundealer",
    max = 2,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "GunDealers",
})

TEAM_GUARD = DarkRP.createJob("Guard", {
    color = Color(0, 102, 204, 255),
    model = "models/player/odessa.mdl",
    description = [[Ask people if they need protection. Guard peoples bases.]],
    weapons = {"m9k_deagle"},
    command = "guard",
    max = 6,
    salary = 50,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Citizens",
})

TEAM_THIEF = DarkRP.createJob("Thief", {
    color = Color(87, 87, 87, 255),
    model = "models/player/t_arctic.mdl",
    description = [[raid peoples bases. Don't need to advert]],
    weapons = {"lockpick"},
    command = "thief",
    max = 6,
    salary = 50,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Criminals",
})


TEAM_PROTHIEF = DarkRP.createJob("Pro Thief", {
    color = Color(87, 87, 87, 255),
    model = "models/player/t_arctic.mdl",
    description = [[raid peoples bases. Don't need to advert]],
    weapons = {"pro_lockpick_update"},
    command = "prothief",
    max = 6,
    salary = 50,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Criminals",
    customCheck = function(ply) return ply:GetUserGroup() == "vip" or ply:GetUserGroup() == "owner" or ply:GetUserGroup() == "coowner" or ply:GetUserGroup() == "senioradmin" or ply:IsAdmin() or ply:IsSuperAdmin() or ply:GetUserGroup() == "moderator" or ply:GetUserGroup() == "trialmoderator" end
})

TEAM_PROHITMAN = DarkRP.createJob("Pro Hitman", {
    color = Color(87, 87, 87, 255),
    model = "models/player/t_arctic.mdl",
    description = [[People hire you to take out other people,
    this job require you to be completely focussed.
    A single breath can make you loose a shot.]],
    weapons = { "m9k_knife", "pro_lockpick_update", "m9k_m98b"},
    command = "prohitman",
    max = 6,
    salary = 50,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Citizens",
    customCheck = function(ply) return ply:GetUserGroup() == "vip" or ply:GetUserGroup() == "owner" or ply:GetUserGroup() == "coowner" or ply:GetUserGroup() == "senioradmin" or ply:IsAdmin() or ply:IsSuperAdmin() or ply:GetUserGroup() == "moderator" or ply:GetUserGroup() == "trialmoderator" end
})

TEAM_HITMAN = DarkRP.createJob("Hitman", {
    color = Color(102, 0, 255, 255),
    model = "models/player/leet.mdl",
    description = [[People hire you to take out other people,
    this job require you to be completely focussed.
    A single breath can make you loose a shot.]],
    weapons = {m9k_intervention", "m9k_knife"},
    command = "hitman",
    max = 2,
    salary = 65,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Citizens",
})

TEAM_HOBO = DarkRP.createJob("Hobo", {
    color = Color(80, 45, 0, 255),
    model = "models/player/corpse1.mdl",
    description = [[The lowest member of society. Everybody laughs at you.
        You have no home.
        Beg for your food and money
        Sing for everyone who passes to get money
        Make your own wooden home somewhere in a corner or outside someone else's door]],
    weapons = {"weapon_bugbait"},
    command = "hobo",
    max = 5,
    salary = 0,
    admin = 0,
    vote = false,
    hasLicense = false,
    candemote = false,
    hobo = true,
    category = "Hobos",
})

TEAM_HOBOKING = DarkRP.createJob("Hobo King", {
    color = Color(80, 45, 0, 255),
    model = "models/player/corpse1.mdl",
    description = [[The lowest member of society. Everybody laughs at you.
        You have no home.
        Beg for your food and money
        Sing for everyone who passes to get money
        Make your own wooden home somewhere in a corner or outside someone else's door]],
    weapons = {"weapon_bugbait", "weapon_crowbar"},
    command = "hoboking",
    max = 1,
    salary = 0,
    admin = 0,
    vote = false,
    hasLicense = false,
    candemote = false,
    hobo = true,
    category = "Hobos",
    customCheck = function(ply) return ply:GetUserGroup() == "vip" or ply:GetUserGroup() == "owner" or ply:GetUserGroup() == "coowner" or ply:GetUserGroup() == "senioradmin" or ply:IsAdmin() or ply:IsSuperAdmin() or ply:GetUserGroup() == "moderator" or ply:GetUserGroup() == "trialmoderator" end
})

TEAM_CRIPSL = DarkRP.createJob("Crips Leader", {
    color = Color(0, 0, 255, 255),
    model = "models/player/gman_high.mdl",
    description = [[The Crips Leader is the boss of the criminals in the city.
        With his power he coordinates the gangsters and forms an efficient crime organization.
        He has the ability to break into houses by using a lockpick.
        The Crips Leader posesses the ability to unarrest you.]],
    weapons = {"lockpick", "unarrest_stick"},
    command = "cripsl",
    max = 1,
    salary = GAMEMODE.Config.normalsalary * 1.34,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Crips",
})


TEAM_CRIPST = DarkRP.createJob("Crips Thief", {
    color = Color(0, 0, 255, 255),
    model = {
        "models/player/Group03/Female_01.mdl",
        "models/player/Group03/Female_02.mdl",
        "models/player/Group03/Female_03.mdl",
        "models/player/Group03/Female_04.mdl",
        "models/player/Group03/Female_06.mdl",
        "models/player/group03/male_01.mdl",
        "models/player/Group03/Male_02.mdl",
        "models/player/Group03/male_03.mdl",
        "models/player/Group03/Male_04.mdl",
        "models/player/Group03/Male_05.mdl",
        "models/player/Group03/Male_06.mdl",
        "models/player/Group03/Male_07.mdl",
        "models/player/Group03/Male_08.mdl",
        "models/player/Group03/Male_09.mdl"},
    description = [[The lowest person of crime.
        A Crips Thief generally works for the Crips Leader who runs the crime family.
        The Crips Leader sets your agenda and you follow it or you might be punished.]],
    weapons = {"lockpick", "keypad_cracker"},
    command = "cripst",
    max = 3,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Crips",
})


TEAM_BLOODSL = DarkRP.createJob("Bloods Leader", {
    color = Color(255, 0, 0, 255),
    model = "models/player/gman_high.mdl",
    description = [[The Bloods Leader is the boss of the criminals in the city.
        With his power he coordinates the gangsters and forms an efficient crime organization.
        He has the ability to break into houses by using a lockpick.
        The Mob boss posesses the ability to unarrest you.]],
    weapons = {"lockpick", "unarrest_stick"},
    command = "bloodsl",
    max = 1,
    salary = GAMEMODE.Config.normalsalary * 1.34,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = "Bloods",
})

TEAM_BLOODST = DarkRP.createJob("Bloods Thief", {
    color = Color(255, 0, 0, 255),
    model = {
        "models/player/Group03/Female_01.mdl",
        "models/player/Group03/Female_02.mdl",
        "models/player/Group03/Female_03.mdl",
        "models/player/Group03/Female_04.mdl",
        "models/player/Group03/Female_06.mdl",
        "models/player/group03/male_01.mdl",
        "models/player/Group03/Male_02.mdl",
        "models/player/Group03/male_03.mdl",
        "models/player/Group03/Male_04.mdl",
        "models/player/Group03/Male_05.mdl",
        "models/player/Group03/Male_06.mdl",
        "models/player/Group03/Male_07.mdl",
        "models/player/Group03/Male_08.mdl",
        "models/player/Group03/Male_09.mdl"},
    description = [[The lowest person of crime.
        A Bloods Thief generally works for the Bloods Leader who runs the crime family.
        The Bloods Leader sets your agenda and you follow it or you might be punished.]],
    weapons = {"lockpick", "keypad_cracker"},
    command = "bloodst",
    max = 3,
    salary = GAMEMODE.Config.normalsalary,
    admin = 0,
    vote = false,
    hasLicense = false,
    category = Bloods",
})



















--[[---------------------------------------------------------------------------
Categories
---------------------------------------------------------------------------]]

DarkRP.createCategory{
    name = "Citizens",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 100,
}
DarkRP.createCategory{
    name = "Civil Protection",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 101,
}
DarkRP.createCategory{
    name = "Swat",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 102,
}

DarkRP.createCategory{
    name = "GunDealers",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 103,
}

DarkRP.createCategory{
    name = "Criminals",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 104,
}

DarkRP.createCategory{
    name = "Hobos",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 105,
}

DarkRP.createCategory{
    name = "Bloods",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 106,
}

DarkRP.createCategory{
    name = "Crips",
    categorises = "jobs",
    startExpanded = true,
    color = Color(0, 0, 0, 255),
    canSee = fp{fn.Id, true},
    sortOrder = 107,
}
--[[---------------------------------------------------------------------------
Define which team joining players spawn into and what team you change to if demoted
---------------------------------------------------------------------------]]
GAMEMODE.DefaultTeam = TEAM_CITIZEN


--[[---------------------------------------------------------------------------
Define which teams belong to civil protection
Civil protection can set warrants, make people wanted and do some other police related things
---------------------------------------------------------------------------]]
GAMEMODE.CivilProtection = {
	[TEAM_POLICE] = true,
	[TEAM_CHIEF] = true,
	[TEAM_MAYOR] = true,
       [TEAM_MEDDY] = true,
        [TEAM_SWAT] = true,
        [TEAM_SWATL] = true,
        [TEAM_SECRET] = true,
}
--[[---------------------------------------------------------------------------
Jobs that are hitmen (enables the hitman menu)
---------------------------------------------------------------------------]]
DarkRP.addHitmanTeam(TEAM_HITMAN)
